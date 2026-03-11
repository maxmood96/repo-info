## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:1386b39e44975fb078f09141d70bb83fe1526a44698f7d752b93c104348b4014
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:c99b4232a52ba9a17a4aaac82fa5b6a294e47ff3f007318e7d5d09c66997f47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430914021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ef12f86bccb91fb6d070a58318c32a351a975cd12cffeebc69f249e66afa17`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:51 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:32:51 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 11 Mar 2026 19:13:44 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:13:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:13:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:13:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:13:44 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:44 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 11 Mar 2026 19:13:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 11 Mar 2026 19:13:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:46 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 11 Mar 2026 19:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33ed62a416a2f01405e82800e2dbefc0c3a94e9a848076d6d1af5b54ab21145`  
		Last Modified: Wed, 11 Mar 2026 18:33:12 GMT  
		Size: 153.4 MB (153362775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a545bb865160943ef10ce9bf70c561cfbb93e508587243c2ff1d1377bf6e7`  
		Last Modified: Wed, 11 Mar 2026 19:14:15 GMT  
		Size: 86.1 MB (86073300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dbd0c46b13063d3560ca0cf4ed25d0ac79fe2d8fb3cc302395c79318c7f5c`  
		Last Modified: Wed, 11 Mar 2026 19:14:12 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f891f558a28b8a96dac6a3fd5b9cad7c89d1dff8d4ef4d3a679fdf516d65bf`  
		Last Modified: Wed, 11 Mar 2026 19:14:16 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03455ab17c791f264cc4c78e7d91587781ad965a9e87dc9c04834052b4e4b47b`  
		Last Modified: Wed, 11 Mar 2026 19:14:12 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5cb77dd35bf62fc8c919ecf535a4106991f87c6cf4f87dc48ba30f0e91feac1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34728fc0a9c9f935d973c991fc58fb7b33af9b0251c479ed62d790d7d65ca8bd`

```dockerfile
```

-	Layers:
	-	`sha256:4a5838c8cd37fed03058cbcf9dbbf6e124361c3be3292a5b3f90f33f52a34552`  
		Last Modified: Wed, 11 Mar 2026 19:14:13 GMT  
		Size: 11.4 MB (11366081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7bf101eea1b059489cf04cc6a4f1bfe6618536469aa1b5b61cc2eeab716988`  
		Last Modified: Wed, 11 Mar 2026 19:14:12 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:eca91214b60545e71e341bfd4a93f3fcd48bdfd1259870fcf69788f5572fd569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.9 MB (427864955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6c9e9111bf666d1fe5a55a088c2f5434f318cc49ea693179da29347ffd1751`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:38 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:38 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:32:38 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 11 Mar 2026 19:14:10 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:14:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:14:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:14:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:14:10 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:14:10 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:14:10 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 11 Mar 2026 19:14:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 11 Mar 2026 19:14:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:14:13 GMT
USER gradle
# Wed, 11 Mar 2026 19:14:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 11 Mar 2026 19:14:14 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bda13546ee5a0563ccaab74d7a4ee9419b088a14618b9ee9c4580006c3017e`  
		Last Modified: Wed, 11 Mar 2026 18:33:00 GMT  
		Size: 151.9 MB (151925032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27364e4a2896ee9924f46bdcdfa46600404d7004b5fadd7af82c33ebf4ebe453`  
		Last Modified: Wed, 11 Mar 2026 19:14:45 GMT  
		Size: 85.5 MB (85549065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5380262b8adae53615b4abfe996704af6112dce50528857cc1fff0bfc5a3898`  
		Last Modified: Wed, 11 Mar 2026 19:14:42 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126c0cf25816863ecebc1ad1f83a4559d1bc087c556b3e0097ef8444ed9dbeec`  
		Last Modified: Wed, 11 Mar 2026 19:14:46 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d5e9f4b02dbbd1322ac1b12347a2d7e25370345c2a89660fe3bfe10e58c9be`  
		Last Modified: Wed, 11 Mar 2026 19:14:42 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5f7b60f61033df03fd8bcd0905a21fe3686edd64692ab72bbb7665ecb84a9b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1038ffdd2d588312907f0dedabed030e4bb5c87e10dda89540fcbe91b12f86da`

```dockerfile
```

-	Layers:
	-	`sha256:0e7412d591a0bfecadb90456e3ca8622eeaa1ffd185bc81c10304912be1c9a52`  
		Last Modified: Wed, 11 Mar 2026 19:14:43 GMT  
		Size: 11.4 MB (11365924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab653b46b18164bd023dcef3b9018310746ffd01c2fdaf4005410ef31bbfca6`  
		Last Modified: Wed, 11 Mar 2026 19:14:42 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
