## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:ed068bc774f2fdbacf40327072c3a80b76475d16b36d9c9c4b9baaaa2ca744b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3a10f4b75e520696ca03708b9a13aaf3af154a521f6d5b5cd3cc4970392ccbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171883728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b948f0168aae46c28fd6fdb272b01b24fc4f8deb56929ccd8d4f86e9200e41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329fa2e8f86e6d9c3f2b0bf17a57b609d52a7d58d1fdd0c144c59f4ce7cb6c6a`  
		Last Modified: Tue, 20 May 2025 02:14:17 GMT  
		Size: 109.1 MB (109123743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb3f3dc2570bade25d8687924d68ab1723562bb7043b97003b517daa024cdb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dd387f5725663e1fba74582bc32e491d15ba38cc25034313d8e6890689a855`

```dockerfile
```

-	Layers:
	-	`sha256:239ab8c6478e330c601a2353736267676a6b367586493f528edf1ea337394a51`  
		Last Modified: Tue, 20 May 2025 00:50:48 GMT  
		Size: 7.5 MB (7499678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f055d63edbf0d3fb3cf3d91f9dc516533f5bd6e4ad9fc7a082fac1979d37d62c`  
		Last Modified: Tue, 20 May 2025 00:50:49 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cacaa08d3e37b56d342305ac4f52304da19c70bbfe2058c997202812c2d2e2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552f3c625822e0e6fbfaeede93f5a8f098b4ed6458c525536cfc08b73a752212`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a50a70a0d7849b55559512cd181392ec5d9717f8ddeef52ce60ac6a800e7b`  
		Last Modified: Mon, 19 May 2025 23:48:49 GMT  
		Size: 52.9 MB (52939775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bba35cb1ee7495764aaa06acc849e48be862a58398e37c5f0953a923a2f88908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88de55009da9d2b2c063c5f9b7c2a418008d59bad9a2f3a989e341782971276e`

```dockerfile
```

-	Layers:
	-	`sha256:603bb347eb4a653c35fb3fee87b3d5a3da7013867cb357de85d28d368a3213ac`  
		Last Modified: Tue, 20 May 2025 00:50:54 GMT  
		Size: 5.6 MB (5614453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a265d961fdb102e5cb6796a8af60d6f7a008da16917c1510770acfa4c58fe8`  
		Last Modified: Tue, 20 May 2025 00:50:54 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.in-toto+json
