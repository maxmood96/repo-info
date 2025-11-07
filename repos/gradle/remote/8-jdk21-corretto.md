## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:6c3a99b7cd76d58a1466c0a1409f90de576f58888e7db529a25284243b013680
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:96d3514d18b1203817b11f2b6d5a5ec74883c44ddcd9446bdd244ed32981747c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.3 MB (447283221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c520939d3b32ddac46813c51e9189e511c94da39b6231495fca4ea26f92fcd`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:16 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:16 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:06:16 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:06:16 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 05 Nov 2025 04:51:27 GMT
CMD ["gradle"]
# Wed, 05 Nov 2025 04:51:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 05 Nov 2025 04:51:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 05 Nov 2025 04:51:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 05 Nov 2025 04:51:27 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 05 Nov 2025 04:51:27 GMT
WORKDIR /home/gradle
# Wed, 05 Nov 2025 04:51:27 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 05 Nov 2025 04:51:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 05 Nov 2025 04:51:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 05 Nov 2025 04:51:29 GMT
USER gradle
# Wed, 05 Nov 2025 04:51:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 05 Nov 2025 04:51:30 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d298c96cc089701668f1f26ebc2ed62153aa52cd816ed6691a3e4aa37f8b318`  
		Last Modified: Wed, 05 Nov 2025 02:50:01 GMT  
		Size: 170.2 MB (170217752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a659b1be5adbd1b1d0fcf1b3ab0ec66ea82a47fac81ca2186ef347383a124a`  
		Last Modified: Wed, 05 Nov 2025 04:52:24 GMT  
		Size: 85.6 MB (85612445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c36fa3f082073b24fc02f27f570c5eb054db7c9ee5b54ccde205a2ecc8e6d`  
		Last Modified: Wed, 05 Nov 2025 04:52:11 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb8686f9e9c0fa439df6198949a082fecb0e33b456abc853e63c82dbad00cae`  
		Last Modified: Wed, 05 Nov 2025 06:27:09 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c768878c920788a825df7309a1a220f6b439a3b2427062e0ff3f155365c6e36e`  
		Last Modified: Wed, 05 Nov 2025 04:52:11 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:af34f2d491eee0ae8595e6e9bdc1f7640d129ed699de93dfe71a4beeeb384324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11341765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b292367c6381ac5b59b34703eab0a296f2da6b8ff1421264c5b9e60ee5a1bd9a`

```dockerfile
```

-	Layers:
	-	`sha256:db31eb18b056316b2a151a57b9449643bd4b5f6115151b15ee0c699bb2f4d874`  
		Last Modified: Wed, 05 Nov 2025 06:19:21 GMT  
		Size: 11.3 MB (11320884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdae48a175a2c7550bd0d59e440d03c6b426c9d745aa47138836bd3e6152e9aa`  
		Last Modified: Wed, 05 Nov 2025 06:19:22 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9b0b7543223f19b26885a78ee3bd69b0a4fa7f083ab0373ade97a9f8632d3258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.0 MB (444001062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aceee08b2481eb33788a812cf631a7798f21de81742edada4786e3bf33ef18`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:23 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:14:23 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:23 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:23 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 06 Nov 2025 23:11:59 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:11:59 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:11:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:11:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:11:59 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:11:59 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 06 Nov 2025 23:11:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 06 Nov 2025 23:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:12:02 GMT
USER gradle
# Thu, 06 Nov 2025 23:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:12:02 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc78c02c91f4f2038e786f731208f8cc3446308a4d3f914fe9891f94f2eb9e`  
		Last Modified: Thu, 06 Nov 2025 23:11:22 GMT  
		Size: 168.5 MB (168474554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b383ed50f3eb62cd580a5ad564e5229174de3aca523e0652a35da1f35956c`  
		Last Modified: Thu, 06 Nov 2025 23:12:58 GMT  
		Size: 85.2 MB (85168445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdd07a3ef82b08be36c41e4698fbcdf4eea85b0e290cf479440ef216bb65c9f`  
		Last Modified: Thu, 06 Nov 2025 23:12:48 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14db191b91c9e25cdbf78bfcf23443a5e554fe7a21db76722281a266bf37181`  
		Last Modified: Thu, 06 Nov 2025 23:12:37 GMT  
		Size: 137.4 MB (137395173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0bfadfdc11149f45125d53393e56f91e4420742b771faaa6254f1102ef6779`  
		Last Modified: Thu, 06 Nov 2025 23:12:48 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f9248927fec3061df8ac1f1c717a211a17afc68b5596fb26e97ade63da0df15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11340916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a472d5d0fa7a928f1140ebe52fda039c91f90920f065f266606b26e949742`

```dockerfile
```

-	Layers:
	-	`sha256:22f3e29da3b4d413e143b9a3e3a10748c04d0adf68aa08a32e910cc82a35d7ed`  
		Last Modified: Fri, 07 Nov 2025 00:21:37 GMT  
		Size: 11.3 MB (11319862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f17a275d2445a89182e7944fd1aab00f9b4f41c1632f9c315dcef870fe5b65`  
		Last Modified: Fri, 07 Nov 2025 00:21:38 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
