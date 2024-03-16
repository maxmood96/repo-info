## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:cd387b0a5b556ce08bcb069f2c5531a54701166bcdd957f8f7e468672363d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c7eb1c5c6ecf25b6fbfb1061e1862ae19b3bad19d6ae9552b699c8106818736f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.8 MB (392792379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ea54a13527fa6f3aefc5463963dbfb9a9dd287dbce2d17ec353c9b8a0cf65`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 07:58:56 GMT
COPY dir:a3b34d0fa41c44f27db0e1cc5fb85c42e2d376f97e37c993883bc79b0ac16bdc in / 
# Sat, 16 Mar 2024 07:58:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:31:34 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 13:32:08 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 13:32:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:32:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:47a7782bf36730e29aeeeb2bd36b1fc2a9d8b97f2ee4990a6ad2300602de69b0`  
		Last Modified: Wed, 13 Mar 2024 20:11:15 GMT  
		Size: 52.3 MB (52334338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756f094c9163b2b310ce04251d35d93a738b68c19d1947f6200fcf305cb40016`  
		Last Modified: Sat, 16 Mar 2024 13:45:07 GMT  
		Size: 278.3 MB (278325173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400e22833aa687504df2538a4db15fbe189b3c359b7f1637f75b0781986c370`  
		Last Modified: Sat, 16 Mar 2024 15:05:50 GMT  
		Size: 52.7 MB (52651543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28d176a93670f5e227a45b4382a9480d87736f090039557d562597393311953`  
		Last Modified: Sat, 16 Mar 2024 15:05:48 GMT  
		Size: 9.5 MB (9479940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d45093813a46d3a26cbadea8c9044e4c05b84c1779ef37fdc6c824643578335`  
		Last Modified: Sat, 16 Mar 2024 15:05:47 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea595b163469506f028f9574d144a1d6121fd906fafc69039fe7c1629af710d4`  
		Last Modified: Sat, 16 Mar 2024 15:05:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c7a9653cb62a5eb8f4c643124b06ec41210d86c350cceb8ac487bb821f7a1`  
		Last Modified: Sat, 16 Mar 2024 15:05:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c7fd344b52e7850e99551b736e9613f0ebf6b15e5b503bd730cc2f42c4ada5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230199573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5334e26594b69370c7c574674597bb22d87eae4923b418d4d5d77d94a3d289`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:37:23 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 03:37:41 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 03:37:42 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:37:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a6f92ab4e9f3baaede015c170c432a22e3070333294a6d79f04844fdcfd103`  
		Last Modified: Sat, 16 Mar 2024 03:50:23 GMT  
		Size: 118.6 MB (118562695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864ad54fbcb4027c3e2a5066cc08c079688c5dcfdba8f93d8eda67c14a6a87fd`  
		Last Modified: Sat, 16 Mar 2024 13:05:27 GMT  
		Size: 50.7 MB (50740986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ad00fd01cfa5885868285e32faa697c953ed022bb1674ea1ea1e9c08c12cf`  
		Last Modified: Sat, 16 Mar 2024 13:05:25 GMT  
		Size: 9.5 MB (9479926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc852c1e03ff9e405f3b3bb798e2bbf3a81824b28b2ed8b747a1c3e92757c31c`  
		Last Modified: Sat, 16 Mar 2024 13:05:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ca23f64f04f26bd992517fb62f656929b7c4625e6a2a4795a138cbbebf03e`  
		Last Modified: Sat, 16 Mar 2024 13:05:24 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1982dd449c85c25c9309149bb6b73474e74ba95fc8bd9212950ca671fee33b5f`  
		Last Modified: Sat, 16 Mar 2024 13:05:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
