## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:e13a86f0ec2f2c42a1dea5ac06b327b211f77643fb8cc6d05b5ac1f77c73a5be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:839ac466aea9e7e88b0766a989365780356505677d4ed3629da80cf8ebf06983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187903175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d972c8285c007ce5dcf8f2f6e88b0f0b4bb4e53e6ec3bf0965cf9d703586f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ae7543d45fc657d84c8ff2d00db1221caad6e0b6accb05bda211e24c5d270`  
		Last Modified: Tue, 24 Sep 2024 01:56:54 GMT  
		Size: 125.2 MB (125224641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6793b950d38235e07b6cc356f08106553777f9b81cb904e71cfd22ad4e62259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ffa9a9bff89093325c14d29b914b0e0dbaadda86fd95f189538b396f025db5`

```dockerfile
```

-	Layers:
	-	`sha256:4eb531945df5b51a97d690875ff96995a5a43270b3b5bab7104e11269edaa31a`  
		Last Modified: Tue, 24 Sep 2024 01:56:52 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e830d2e7581b19551428ff11c1dc5445c245d6740b89fd9c932da8870f5f1fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132120270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bb11c5047a16770cbf217047e74a3c061b68dfa2b4fd4c0f2e04dd9ba46b10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4ec3312c4f47e9e0501b7088819738cde850a70e5a729d5e6adc09ae8fee7`  
		Last Modified: Tue, 24 Sep 2024 02:28:55 GMT  
		Size: 67.5 MB (67533723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c45539f9a5e45d085b583851ba988db53ddd1fe683d28994d25df5bbf4abbe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587c2015f932877a3be9809052d47e0f19117e5aca9d7d0e548bb9605de56be3`

```dockerfile
```

-	Layers:
	-	`sha256:6093a6c7ff4b14d71530efad0d3d6dcedb21f440277e6b7b5d5b8ccc1d657c72`  
		Last Modified: Tue, 24 Sep 2024 02:28:53 GMT  
		Size: 6.1 MB (6077709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5d826254f73f70f4284e1b4690a2fb3088a6a657639ffc738cba497fd8c14c`  
		Last Modified: Tue, 24 Sep 2024 02:28:53 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json
