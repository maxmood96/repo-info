## `amazoncorretto:8u472-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:479dd6ccef9547e4a86d64238b34bf69fa0e0921a4bb61c3c6ad3dba2ea4e1f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cb6ccedfce11c77849933de407517142d0566a5f67af14e5ff405b4c8e2fbe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172056805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77729d8196029f43c5ee45af2ec5ce8d5f9c3ab30f7e14755758f9180824a0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=1.8.0_472.b08-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36718231a8c898b6667489e5e2d1cdc2133c4dc1df962f2498bbcb4dbbde31fa`  
		Last Modified: Tue, 21 Oct 2025 23:26:33 GMT  
		Size: 109.1 MB (109116185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f898bea55cc2c533f9be73abd733080707eaea54e1a665f102a388a1a7ecef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d44966bf6d5afd4db9740a83b5ca7fc6dae268fb113776d85407d712729e4`

```dockerfile
```

-	Layers:
	-	`sha256:7d11784d397746bb3fbd3d9814d1f586d50df43314e5fa341a8876d62f486bd2`  
		Last Modified: Wed, 22 Oct 2025 00:55:07 GMT  
		Size: 7.5 MB (7504128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03806411fb9386d9b75396dbb2c3f2fe1fca5e9b6fd40b9b284b22ef94a8229`  
		Last Modified: Wed, 22 Oct 2025 00:55:08 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:656359dad6f22fbc4d7c2667dbf0a45c77600319a2aca65fdf8c72fa301301ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117733298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907fa2c8a1b8de6b54770167d926143390845b3c676a484113b0b0f069b5dd85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=1.8.0_472.b08-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a89ad473b24bfb84029acdb9c71f3024f0160192f1eb3b8a9a93c521d038909`  
		Last Modified: Tue, 21 Oct 2025 21:48:55 GMT  
		Size: 52.9 MB (52940090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b5e31331b7a4c25f08f2ffecfe3f89c394f65d2866a3c8d728a13bab3e363002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1725401a12064bcac1a960b5fddf6d89c7696362411efb8faed612f951f820a9`

```dockerfile
```

-	Layers:
	-	`sha256:204a873e9a1046b2e96625e2c25f46e2adff0c1bd5349cc990a63b18389accc8`  
		Last Modified: Wed, 22 Oct 2025 00:55:15 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b450fad0af5da2ecd3dcd9f9969a59168d17bccdf46d0186f557b1d763efadef`  
		Last Modified: Wed, 22 Oct 2025 00:55:16 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
