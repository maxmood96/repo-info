## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:4c42eee648a1d1921c99a76582569df067942b862099d8237600f3875079e7df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0ae54f6ea043931f8c36ed44d845ca5bb53bf8bfb44e0aa3e76cc77a35733a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196013423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b3256a453d2723713abdad7e3f07ed34da079eb161f21717d80f3511257170`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1100df2754b7ce890fcadd168ab1fd6f010fcb37ba60659e87e6f8c8188b88`  
		Last Modified: Fri, 20 Dec 2024 22:31:07 GMT  
		Size: 133.3 MB (133335984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:01e63e06110244919d3d128a0282188134ea63aa1cdbe984228207d88ca523c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35d8b06b7e42d5892257ee7957ac0e1e136fee24190aa972260c47e72456997`

```dockerfile
```

-	Layers:
	-	`sha256:98280e11e6aafc993fcba607a65a804b7b356b613a298f6aee1b1ee144a688eb`  
		Last Modified: Fri, 20 Dec 2024 22:31:05 GMT  
		Size: 8.0 MB (7956590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76f3ad41bfc3618b0f04f32b498ea58be5003db5b4d07d0c203647fc2267f73`  
		Last Modified: Fri, 20 Dec 2024 22:31:05 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b211dab8d15521dcd93e165d6372caa456516741a57fe3c08d6997f898f93782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140815347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3c4c0ccd09cc6f9f260c8e661211eeeee03d626d3fa75d6263c23b9b45afb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcb4960e3eabc5ff5a5a0d6f92f07e9a944873a77897836877a58e26da8743b`  
		Last Modified: Sat, 21 Dec 2024 01:37:12 GMT  
		Size: 76.2 MB (76233460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e1421a88dd6d4ac9a3366c83b09c6289f699af72d4395a1359d238a21207d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93ecb3c259fe5135c7b6286d7e79c1162e448ec3e5e66a237e164ac8de12a5`

```dockerfile
```

-	Layers:
	-	`sha256:8b2e10688f1513c424471115c4411cabe8114a04a7417900c22c66152584b938`  
		Last Modified: Sat, 21 Dec 2024 01:37:09 GMT  
		Size: 6.1 MB (6066675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea010b16b3669ebb87598da4e958e2b0bc8be9eb77417b50e333f920a4646eb8`  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
