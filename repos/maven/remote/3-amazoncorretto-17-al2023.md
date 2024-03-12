## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:a282ba01174c167843e90e228e5c4713f2af497acb997e48f7a041483f289a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4c8bd9ec72b372f587f7b9d92564a307e4f5180b7ec08455fb346617bae1757e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268694114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2aaec9afbda01e8c1dd2c532bd6ad7fa8af31f9eb827297596a59c4a7cfc50`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:15:24 GMT
ARG version=17.0.10.7-1
# Mon, 26 Feb 2024 23:15:24 GMT
ARG package_version=1
# Mon, 26 Feb 2024 23:15:50 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:15:51 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:15:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4064348825fc397fd1bb494cd3f0f56f9da72e50ab9b77522bb78f046eb9186`  
		Last Modified: Mon, 26 Feb 2024 23:27:50 GMT  
		Size: 156.8 MB (156849569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0660ced903a792379913e14c9588dcde4c75861c1c37871fbdc24ebc38b2a3b`  
		Last Modified: Tue, 27 Feb 2024 00:26:37 GMT  
		Size: 50.2 MB (50153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c2c63a1e30792773415a20db000947a4bf1e7347862358c44c9634a72f893a`  
		Last Modified: Tue, 27 Feb 2024 00:26:35 GMT  
		Size: 9.5 MB (9479927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a959d6077cbb2082fc229a2b663db815604e40f2955771127ff963c6396fac`  
		Last Modified: Tue, 27 Feb 2024 00:26:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a30ad927d89ef92c3cc1e3b0855ce2fa1ec532ca96b41abb6aae5254501b1e`  
		Last Modified: Tue, 27 Feb 2024 00:26:34 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620892dee95ff153f45df9acd5cfd0ecae55f8e0fad054c095ef89e6e5515e7c`  
		Last Modified: Tue, 27 Feb 2024 00:26:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0b11e419e18dfa6d068198339324a108309836d2968b320c50877716588be954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267178458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b998c31a6f321dc98cfd5491574d5d6608e877f7b1d7d150ac2b018821d03213`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:43 GMT
COPY dir:2bac3e0f2f9808be2259a0eea507562cc31d6f7cf5f26809139e8bb63fb6b535 in / 
# Mon, 11 Mar 2024 22:39:44 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:14:50 GMT
ARG version=17.0.10.7-1
# Mon, 11 Mar 2024 23:14:50 GMT
ARG package_version=1
# Mon, 11 Mar 2024 23:15:08 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 11 Mar 2024 23:15:10 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:15:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:89bff426afee4c835c6855932ea2864aef333271964dcfe8c4e0cd4be90649f8`  
		Last Modified: Wed, 06 Mar 2024 01:18:22 GMT  
		Size: 51.4 MB (51406909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0487aeb5780c8a1d0d5424a93ec9a154d2b696ba83bb92adc22d44c802facd7a`  
		Last Modified: Mon, 11 Mar 2024 23:24:22 GMT  
		Size: 155.6 MB (155589839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2848b2eab6730dd22a00594ec661655436f64aa10b9f672abbc8da47740e5`  
		Last Modified: Tue, 12 Mar 2024 00:20:22 GMT  
		Size: 50.7 MB (50700391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc52987a60833d002c706dbd7b77fad65cfb20fd1ff0daf56f3bd4b86997fc7f`  
		Last Modified: Tue, 12 Mar 2024 00:20:20 GMT  
		Size: 9.5 MB (9479936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a230a0d47bfa6996fa221bd25e3f29be16eee9582ddc60949b8e562e3a94e02f`  
		Last Modified: Tue, 12 Mar 2024 00:20:20 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668cbe1f8fc4959924593508b1934ffd382ba689cce0550a85c30f69882e0d17`  
		Last Modified: Tue, 12 Mar 2024 00:20:20 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344aa6840e07a4140e77b4c89eae4b92eb210c8faaa9d6138e1f44fc8fb82d85`  
		Last Modified: Tue, 12 Mar 2024 00:20:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
