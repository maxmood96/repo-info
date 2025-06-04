## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:14d0dbc42b56db3bdf284003cd10d93dc23c14fe1975bc738e2aeb3d990895ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:dd79259c6ea8121877e818bd6f9ef723b8fa04ef6f14fad9b3184fb4ef0ef565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399316250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4df25a0cf276e5241fc45f11675a5ec3c09fd3478ada6a944521b415d2bcf9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 29 May 2025 19:34:11 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:34:11 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 29 May 2025 19:34:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER gradle
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889e9ac9fc3d45e4907ce0fcf1fdda95e985943f212ff7c433b40b7471c65762`  
		Last Modified: Mon, 19 May 2025 23:45:53 GMT  
		Size: 153.9 MB (153910910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971307cabc3b102bb82de35e6e86d2216176dcfe86479a02c744abd23c20422`  
		Last Modified: Tue, 03 Jun 2025 23:58:20 GMT  
		Size: 83.7 MB (83661011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c0144d3409f898a478541d9f34dafd734449c611557937c2d5d95f7a162263`  
		Last Modified: Tue, 03 Jun 2025 16:18:01 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2465d1769711dd1fd258bf39d1ae55b3a179d92cb5c3bfb3e9154c4330175bcc`  
		Last Modified: Tue, 03 Jun 2025 23:58:29 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73582355a6987f6df95711fc8e069db98b5d5662941cbc6d9738ab7da95e3865`  
		Last Modified: Tue, 03 Jun 2025 16:23:44 GMT  
		Size: 431.3 KB (431284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7f5b7086b457dc9c73120a19807a29acb31ddbc805411023dbb3d0907546850e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11207150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990aa85657a683acd656118220eaa126f3ccddfcd687ee8da4c96c651ea03eb2`

```dockerfile
```

-	Layers:
	-	`sha256:14fb40dd4f305287e5a43710434aa9f2cd1539176d6a0a2c46be2f9c056b2c0f`  
		Last Modified: Mon, 02 Jun 2025 16:49:06 GMT  
		Size: 11.2 MB (11186219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3366f724f8b4df7f9436f53f50576354cf24bece4eed56869c4b37726542c622`  
		Last Modified: Mon, 02 Jun 2025 16:49:06 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3b17a6d7962158983a5d5d76087f101375cc87bb8c07025bde436dbb0f247736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 MB (396359319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86f7b11a3667b9d9eebc57b5c989e339689f44f186bed8d07ec01d24c9a3a05`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 29 May 2025 19:34:11 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:34:11 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 29 May 2025 19:34:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER gradle
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b7c511921905c90e2da7ccd5e55a13dc20d0647295cec48db9cd48880a4519`  
		Last Modified: Tue, 20 May 2025 01:02:47 GMT  
		Size: 152.4 MB (152434450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90443e2e7591cc04cb8fd0e4ac9893f80e76d61494c0abf16332ed4ca2735bbf`  
		Last Modified: Mon, 02 Jun 2025 17:10:45 GMT  
		Size: 83.2 MB (83235788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a012bbdd5a202a0f453b869bf58e5b7424e3c293f10503ca804d1d6abba5d0a3`  
		Last Modified: Tue, 03 Jun 2025 16:34:40 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff13ca264b2cd0f8f33f29f71f1c8b4dd5170ace571c57b153ab61198ccafcef`  
		Last Modified: Mon, 02 Jun 2025 17:40:02 GMT  
		Size: 107.7 MB (107696632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7329e25482dd8409913ca4c6ca31837a176e9e7fcda00279ad3fbbc99a9fe371`  
		Last Modified: Tue, 03 Jun 2025 15:31:37 GMT  
		Size: 425.0 KB (425035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b99a7cf1dd241b5f5192a6804593b1d92c807debf21d972a47ea7e3660b78bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11207142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16a281b42a49daac635209023a701bb7165cad98de9971d8dcf0c5c73db1543`

```dockerfile
```

-	Layers:
	-	`sha256:d17aa1fde66ab14fff752b86270774ecbb4b4bbd14e9871515d33840dc6c6fc4`  
		Last Modified: Mon, 02 Jun 2025 17:40:00 GMT  
		Size: 11.2 MB (11186038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b899373a9cfdf2e3f912906f195972156a032b9fd9069c2df697256e163e8d26`  
		Last Modified: Mon, 02 Jun 2025 17:39:59 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json
