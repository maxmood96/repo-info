## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:d437f539eaa6994afa4a06022146f326595a853e4d3a4ac03ee372631108ba36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:a6c2c7580a9afa3493ee78cd47c1b769243d950df35f8898e06909e1a4100aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351970009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc31feeb33a4697165a2825fc60f1ca704e80d914ad011c5a31badba17f7d2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:01 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:34:01 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:01 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:01 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 11 Mar 2026 19:16:29 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 11 Mar 2026 19:16:31 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:16:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:16:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:16:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:16:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:16:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:16:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:16:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:16:31 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:16:31 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:16:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:16:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:16:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f515facfbc58fdfaa9cdcbd4b5a55791c80be6edda4df3bb9183ca525b464ed`  
		Last Modified: Wed, 11 Mar 2026 18:34:23 GMT  
		Size: 170.2 MB (170192431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16046c988f265dbdfb5b2fc69ea52753f22479889e8f9bee9f031e07df63f03`  
		Last Modified: Wed, 11 Mar 2026 19:16:47 GMT  
		Size: 105.5 MB (105517495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9312e2f573335d78b1db4801c6634819b4ac79ba7fe8adbf5ad66133623c2637`  
		Last Modified: Wed, 11 Mar 2026 19:16:45 GMT  
		Size: 12.5 MB (12528432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342f4ecfc177f4ef042dcb19bf3bcd153534b64c24fa664f73d9da59ffaa2bf`  
		Last Modified: Wed, 11 Mar 2026 19:16:45 GMT  
		Size: 9.7 MB (9697517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba7b7919b95a4cbcb981cd8eb0e4dc680ad138f4ffb22d8ebb2c685554d9404`  
		Last Modified: Wed, 11 Mar 2026 19:16:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44885de131ce7f953bc4bfb3a015780a2ad8baf17bf82026680adde2d804b05f`  
		Last Modified: Wed, 11 Mar 2026 19:16:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c74054a64b8d6f1c06919f4afecfa751af0f3f3d0eb05448a3a8c20a6686fbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e776be97fc1e10d526c0b0eead31caac9f4cf303bb5b2b776b1f0cc2cb241b3`

```dockerfile
```

-	Layers:
	-	`sha256:c94d3b28ce875046305f900d118e6f6f293f6b673e871f4d7fc8ac199f690636`  
		Last Modified: Wed, 11 Mar 2026 19:16:45 GMT  
		Size: 6.2 MB (6240998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e52557faada30c0c772ebd66a66d02a4788597beccd0d9f80376ec616112eb`  
		Last Modified: Wed, 11 Mar 2026 19:16:44 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ce655ba17a4485d2131e20ab5a75506c026cec5f13bdf95887e2ccd1eb497382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348159829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e80e20875f1edb1e99bdcbc4953863d39fcfa0a5d76f48d093d1b5d6200d813`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:49 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:33:49 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:49 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:49 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 11 Mar 2026 19:16:40 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 11 Mar 2026 19:16:43 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:16:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:16:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:16:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:16:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:16:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:16:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:16:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:16:43 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:16:43 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:16:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:16:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:16:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d30746b1d1a0fa8e3ef2fe5cc5ec2c6c146413028b9dd25386bd91e4b836e`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 168.5 MB (168466825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6fe05c4520c33ce7b0c3ef1f2b81ce3441ca9ff6f24d6e19a163dd0d45141`  
		Last Modified: Wed, 11 Mar 2026 19:17:01 GMT  
		Size: 104.3 MB (104263223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e612abfadebedd8949d9c70935919208c53a61bf9d7d3c644ee96aec87e038`  
		Last Modified: Wed, 11 Mar 2026 19:16:59 GMT  
		Size: 12.8 MB (12789807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310f5e74b8e4789da21ba9bf4ac4b809a29a45a29056b21fe150eb2ff10b675`  
		Last Modified: Wed, 11 Mar 2026 19:16:59 GMT  
		Size: 9.7 MB (9697558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549b8441d82aa42b326ac259b2b34f9fcbe664721713929cf9697bc1fe428e7c`  
		Last Modified: Wed, 11 Mar 2026 19:16:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e28cf0f2a5e54d8bead4a79782040fd7d0814e40f6456c20365b5041cab6380`  
		Last Modified: Wed, 11 Mar 2026 19:16:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8916b3ac885f0b2bbb55a4219614a4e2ffc679a7c6327882cdfb4ae9075f8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6258369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52060a1fb4034e25c9cbc3c968b84595fde07486ecba323f1375dd0ecda66bed`

```dockerfile
```

-	Layers:
	-	`sha256:30d16fdcece74451d4575761c12689664c9566e3f000ec13f6a26a2139f48702`  
		Last Modified: Wed, 11 Mar 2026 19:16:59 GMT  
		Size: 6.2 MB (6239931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62ca308b01887f8bba8f73055d71fa04eb1e6ab2bb4d6daaa9c48021f46992d`  
		Last Modified: Wed, 11 Mar 2026 19:16:58 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json
