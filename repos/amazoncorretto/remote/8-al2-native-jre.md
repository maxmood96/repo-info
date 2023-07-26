## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:1278dffbc9b7d9f1352f77e465e5ba613a604098b7d3c62e288a81ac250e7ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd00119b027f2c3d36280472a6af1ff9c84d20075af602b678d76f7842c93e5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171619730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1942629ed7f333dcb9e2b33b9c6c49b2013f2aa1a3fc33c5840e7332daea6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:12:48 GMT
ARG version=1.8.0_382.b05-1
# Wed, 26 Jul 2023 20:14:35 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 26 Jul 2023 20:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:14:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d865871e1c86838c99dfcd76b18bebe0d66e31ae658ba23aae83792437c1bedf`  
		Last Modified: Wed, 26 Jul 2023 20:25:58 GMT  
		Size: 109.2 MB (109167810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8b7130f2e155317fe7d9a1d5dfe6213ecaf4ff8c95daa55e500323d31f4946d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116899858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff654713812ccfa2f1ba9fedcbf7836c015da3c38d89807dcf3701ac984aced4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:59 GMT
COPY dir:680654fa7b59b44a83c6e6e3392ca226b5dd93f22761e5f1147351db4c3466cc in / 
# Wed, 26 Jul 2023 19:40:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:17:32 GMT
ARG version=1.8.0_382.b05-1
# Wed, 26 Jul 2023 20:18:24 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 26 Jul 2023 20:18:24 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:18:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:51a637e5b43ccbed5bec2958dc012693f30cc3c6b3a2760e6d675bedbae44e84`  
		Last Modified: Wed, 26 Jul 2023 19:40:35 GMT  
		Size: 64.1 MB (64129279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806067c1b6ddaa956d70a9bdf3134e1a618acf226cae9084c4658cfafa726890`  
		Last Modified: Wed, 26 Jul 2023 20:27:04 GMT  
		Size: 52.8 MB (52770579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
