## `amazoncorretto:8u372-al2-native-RC-jdk`

```console
$ docker pull amazoncorretto@sha256:5e532e35b7db6e23599fb85bf92b3a829f6a1d4b127709b4b88ba5338da5a030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u372-al2-native-RC-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5fd776c3b4bb9be88c59d63f0ba78f6a2ab6a602a8b3d79da197ba0ab46ca45a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196580089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91632539124720015216fc162c62509875f9943a7cdd4ad032bd20a38e841db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:20:15 GMT
COPY dir:129c77392b447afbaa234a34f434bed5ec790278efd165e1d59d4425216de49b in / 
# Tue, 20 Jun 2023 22:20:16 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 22:52:35 GMT
ARG version=1.8.0_372.b07-1
# Tue, 27 Jun 2023 23:21:41 GMT
# ARGS: version=1.8.0_372.b07-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Tue, 27 Jun 2023 23:21:42 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jun 2023 23:21:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0086aac11276884f299f6c13a98f93369cc50f7c0518989c2d4a29dd999feb70`  
		Last Modified: Fri, 16 Jun 2023 00:07:41 GMT  
		Size: 62.5 MB (62487611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e7b65496c00198340318298c7fe722dc8f7524c18476ab7e53ff628f88f99`  
		Last Modified: Tue, 27 Jun 2023 23:29:00 GMT  
		Size: 134.1 MB (134092478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u372-al2-native-RC-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8468de5582c321f1dd36464bf504be6136e6ea950e975f7cb644b07aebbb5f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129961333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5044e4a1f7590076e297320187f2a86ac7ff9c27442ef115f4f3574aca36a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:40:04 GMT
COPY dir:ff562af1eb403156d540f974a5832a6973c9f08f4a181bdb7b2f5a2faf708d9c in / 
# Tue, 20 Jun 2023 22:40:05 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 23:22:33 GMT
ARG version=1.8.0_372.b07-1
# Tue, 27 Jun 2023 23:42:30 GMT
# ARGS: version=1.8.0_372.b07-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Tue, 27 Jun 2023 23:42:31 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jun 2023 23:42:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:322949bc3f462f25edd57d234e2687af2a359a973c83b2d139df37b10dda65be`  
		Last Modified: Fri, 16 Jun 2023 18:06:42 GMT  
		Size: 64.1 MB (64129772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ad1f2b7f6feccae0b36c091ee7b67280b439da51d5f488e85d5850ea1d3b9c`  
		Last Modified: Tue, 27 Jun 2023 23:47:35 GMT  
		Size: 65.8 MB (65831561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
