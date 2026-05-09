## `gradle:7-jdk11-corretto`

```console
$ docker pull gradle@sha256:c7253d0a12c221198954ba64ae5072ff70022cc01e8e9119c578c4e5756357e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:021505ccb22b28071b19fee4b9021fd1ff47d8bdd8c55ae8c196c55646fbb0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422744075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429b9fe2ed61766c6627f03923221db1a6582bc488bcd8837bed9bdc2f4e0270`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:06 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:18:06 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:06 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:21:29 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:21:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:21:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:21:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:21:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:21:29 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:21:29 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 09 May 2026 01:21:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 09 May 2026 01:21:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:21:32 GMT
USER gradle
# Sat, 09 May 2026 01:21:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 09 May 2026 01:21:32 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e8ef4b5fb927c0c86de92b3247666810672cabd7e058c5262c750d5d34c79`  
		Last Modified: Sat, 09 May 2026 00:18:27 GMT  
		Size: 153.5 MB (153472393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf76f8be2559985f0b1b4dc57b7ae1a96d943f5df8713cb746ed8b2e6a8a5d46`  
		Last Modified: Sat, 09 May 2026 01:22:02 GMT  
		Size: 86.2 MB (86168878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f13fbc11c54af07c2b0e308bdc2c176b857b65f3620f80f186dc6596a3bef63`  
		Last Modified: Sat, 09 May 2026 01:21:58 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3865b90b44a1981efbcc9c51ce9d4e85b069ece806f061293b40e38a91228d48`  
		Last Modified: Sat, 09 May 2026 01:22:03 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe1a2ae18f704ba05d315bdf2414b970d9e14ae8fa14195b98f72ef4722605a`  
		Last Modified: Sat, 09 May 2026 01:21:58 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a6e33dcf9fa517b612884a78dc8816c3070d81cc0d2a986aef0550d5bf84ba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11306545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a948b478795067db71c20c5c8f9e5aa04f89a1a099586502a5bb9d66b12158f`

```dockerfile
```

-	Layers:
	-	`sha256:0531da0dceb61372a000ea067ee0b4490206622ee52ec0bf3598b6f3b3edb8dc`  
		Last Modified: Sat, 09 May 2026 01:21:59 GMT  
		Size: 11.3 MB (11285674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4886a2fd7d28892a503184288fee046ed60c2399e9f7a9a3d7409783232ff95`  
		Last Modified: Sat, 09 May 2026 01:21:58 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fd132dbf3b4590b9499614fffa45afa0c4aa52824cc18615a1583cc46f37bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.7 MB (419697376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6132dab623fb8598d17d6096ce841eb02280f43d6c09900ed95f0eb76c119ce`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:25 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:25 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:15:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:46:47 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:46:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:46:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:46:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:46:47 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:46:47 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:46:47 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 09 May 2026 01:46:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 09 May 2026 01:46:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:46:50 GMT
USER gradle
# Sat, 09 May 2026 01:46:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 09 May 2026 01:46:51 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763299e6b6a5390624676a6a883b80df08afbd0fe328882a6aa37029abd1826`  
		Last Modified: Sat, 09 May 2026 00:15:47 GMT  
		Size: 152.1 MB (152051820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b26f678ccc2ed944ea8eb5f004dc23696de6da6639ed16ef10eac4dca8f8b2`  
		Last Modified: Sat, 09 May 2026 01:47:22 GMT  
		Size: 85.7 MB (85657961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f97ecfa3e613036db9542d464c7672fff5ebe7ac9ade896514fc1afcb9279`  
		Last Modified: Sat, 09 May 2026 01:47:18 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4091f143a343b5775e2a319c9165338c892dc9b4607dc7b3400f373d4d96664`  
		Last Modified: Sat, 09 May 2026 01:47:22 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d232725991078983ad836527503f967ae1c63a8ef30ec448c719363f5f4a49`  
		Last Modified: Sat, 09 May 2026 01:47:18 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:109423e208a39876f08c4ce9c2f466f1b44a094bd1b9f0a5c9bd32568cebf087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11306537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a424ed6c6ece26b9ad0170e2438ca506de75de4bf0ba7df5479657876407c9`

```dockerfile
```

-	Layers:
	-	`sha256:6bc1722729c3eb53c58bfa7c89028eadae631c9cee46e82ce92179849f4b03d2`  
		Last Modified: Sat, 09 May 2026 01:47:18 GMT  
		Size: 11.3 MB (11285493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59cb2c7535013b94c3dc8c4b6eabd70d583befc9f7ff9f1dd0131d545aeac41`  
		Last Modified: Sat, 09 May 2026 01:47:18 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
