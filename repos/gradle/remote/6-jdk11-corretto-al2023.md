## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:a5a64f6eec7f0e4450f69c5c4d1a4ab313363f71bb2f2a6a1ca457d811c0b854
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:4fa784a8daea20ff56faa8d679cf7ada7831d574904901ba3be6ff58ffec3d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 MB (388540745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c4c124d3d8bfac83ca6ca3c0a62e966d9f670f565bbb70d0196a325decbf6d`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ARG version=11.0.27.6-1
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443f03863f28edb96bdb90c5b660ff341408e95ef072a0f347e5599cc68bb763`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 154.0 MB (153996447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74204c92e05837beec24eaf1b5e0dbb0f7bba4315c0ec54a248fe9cfb1f817db`  
		Last Modified: Wed, 16 Apr 2025 00:08:34 GMT  
		Size: 70.5 MB (70507636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1667148f425afa511c330be60163a1d9bd9f44cfa5d2de70833e91e48620558`  
		Last Modified: Wed, 16 Apr 2025 00:08:32 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7396829835f3682ec38db1f1b610cd88a59b481559c44e8f98f688a3f51d3e`  
		Last Modified: Wed, 16 Apr 2025 00:08:34 GMT  
		Size: 107.7 MB (107696648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d0807008d37191cfb7f4fe26dc552c7a91a6e13775e8d26e697f2df48054ca`  
		Last Modified: Wed, 16 Apr 2025 00:08:33 GMT  
		Size: 431.3 KB (431284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c71612c8c789c0a05793b1c71cdf95d2f40e45461bdff31c56465431864d9641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10689670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7841cb226b570710ce3b386a52c1d84243f2cd656fd3347fdb9db07ebd14d4a7`

```dockerfile
```

-	Layers:
	-	`sha256:a238c3e0a1dc41b644319f56e81cefb5e9161bdc849b7884475e8fe2b32d563b`  
		Last Modified: Wed, 16 Apr 2025 00:08:33 GMT  
		Size: 10.7 MB (10670416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3695ea11b7c00dd0a984b274efa29a29006cefe171eefa7ff26541ea197a021`  
		Last Modified: Wed, 16 Apr 2025 00:08:32 GMT  
		Size: 19.3 KB (19254 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b82c8a8d6eeea63de159254e20e3ad6223509d528f466e71d3df90e581aa07ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 MB (385570249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dedb5d4fadf2da12b8797c774a8fb6d5f6c673a8c4986cc038ebc7852812b26`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ARG version=11.0.27.6-1
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75630dc65e434426bf5e86f59d38cfec76d2e08355e512a5a53a986bf2f549f`  
		Last Modified: Wed, 16 Apr 2025 00:02:09 GMT  
		Size: 152.5 MB (152512317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6062e668dff1c9c962be310c49d5843ac22862485a239d0aa32a95d98235e6db`  
		Last Modified: Wed, 16 Apr 2025 00:26:43 GMT  
		Size: 70.0 MB (69973544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac9df733bdd17f71dd9533fc2803d1320b74345e60eeec397984a0d514a15f`  
		Last Modified: Wed, 16 Apr 2025 00:26:41 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b52bd5399576c5cea6120b8715006a61b239988e8460419b10aae82574ce6`  
		Last Modified: Wed, 16 Apr 2025 00:29:48 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfde9ecd0916571c4e62d3265f7ad3ef79c0effcac8608ebf6a7a39734a8b2a`  
		Last Modified: Wed, 16 Apr 2025 00:29:44 GMT  
		Size: 425.0 KB (425036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:bcbe1b11eb68d4b773524be179251aeda01427f4c281655702ccc95ed3c0a13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10689662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29533c4514a3fcafe5ae6093d4152511f7fe8e94e77fd415b0d495a2ce5ee08`

```dockerfile
```

-	Layers:
	-	`sha256:bf5f41442ec71b78b8604839293842523776be61201ac378d6f9c74ac1bf13d6`  
		Last Modified: Wed, 16 Apr 2025 00:29:45 GMT  
		Size: 10.7 MB (10670235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba9ab49b86b1af463e37341f97eaf4e50bbe4beeb21cd30819b8c78b32af89a`  
		Last Modified: Wed, 16 Apr 2025 00:29:44 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json
