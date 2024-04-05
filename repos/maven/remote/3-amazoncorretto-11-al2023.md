## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:8ca43cc9d12fae5328ecf3073911c4595a771f91d8af64c4d87679b607b5fc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6a56309a71410737f8d25d8903290077616ec47728d396ec170baa09077f97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266587113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f56fcf0955b2c66828a9608b259c2e8a36a31073edb884576c7034580938a8f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 07:58:56 GMT
COPY dir:a3b34d0fa41c44f27db0e1cc5fb85c42e2d376f97e37c993883bc79b0ac16bdc in / 
# Sat, 16 Mar 2024 07:58:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:34:42 GMT
ARG version=11.0.22.7-1
# Sat, 16 Mar 2024 13:35:03 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 13:35:04 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:35:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:47a7782bf36730e29aeeeb2bd36b1fc2a9d8b97f2ee4990a6ad2300602de69b0`  
		Last Modified: Wed, 13 Mar 2024 20:11:15 GMT  
		Size: 52.3 MB (52334338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85208dd5322e7080ccfd2127756409a3a144d4e17936c08151aba687a395c9e7`  
		Last Modified: Sat, 16 Mar 2024 13:46:51 GMT  
		Size: 153.6 MB (153589984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc4742110e0b9635ef58ae69aed066028c5d30dcdd386c773103d6fa0305f32`  
		Last Modified: Sat, 16 Mar 2024 15:03:51 GMT  
		Size: 51.2 MB (51181464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42940656429b89ae790e0e79d5b34261ba319abe6c80a7b7667fd3eea05870e`  
		Last Modified: Sat, 16 Mar 2024 15:03:49 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6aba21ed46b76e1bdf286440cb85a84eee1eed6a6e4472c99faa7664c4244e2`  
		Last Modified: Sat, 16 Mar 2024 15:03:48 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a858a295f20a6821c7541b19508977453cc7c4fcbffdfe031b7e3b7ba74654c`  
		Last Modified: Sat, 16 Mar 2024 15:03:48 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5abc232a947b0c6bcfc423bc5fb72bf1ad670f0db69dfffb8004b535fb54cb2`  
		Last Modified: Sat, 16 Mar 2024 15:03:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5dc22a03873f71a03eafeac34b8db7bf4894b9ddc24e1be3a7057952329790c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258573758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d582f8d2709294a6c203dd6c1ed5b52fc6638365af6187d10a00b4689f1ce11`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:45:18 GMT
ARG version=11.0.22.7-1
# Fri, 05 Apr 2024 18:45:37 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 18:45:38 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:45:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2d94754b29b09d36d06d7091ff3238875614c07c4bb6dbb5b80f212740fa81`  
		Last Modified: Fri, 05 Apr 2024 18:57:18 GMT  
		Size: 152.0 MB (152041201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206aea4acef092da9bcc7e729352646b3abfb05d0a607ab619be1e55a93308de`  
		Last Modified: Fri, 05 Apr 2024 19:40:13 GMT  
		Size: 45.6 MB (45642888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721230b06acd48c79d5ff426ac3467f93c8ea26206604504fe63747f23e7950f`  
		Last Modified: Fri, 05 Apr 2024 19:40:11 GMT  
		Size: 9.5 MB (9479960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85479122595d6aecfa2e3be1820c52e9e213f2f5bd94480f1cb29cdc11b597b5`  
		Last Modified: Fri, 05 Apr 2024 19:40:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f498c2364dddfef0b83f1a35f67f3c731670f820be143a203bbdb1e2e918e`  
		Last Modified: Fri, 05 Apr 2024 19:40:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15472118cb2649b0b0e8bae746d9b93174a4df46cdf1a2bade4a439c28362444`  
		Last Modified: Fri, 05 Apr 2024 19:40:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
