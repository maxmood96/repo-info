## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b95c8fa7b5fdc0d5014d76b8133230aeed9e91274c8a0380925ed39b680b7c5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7181c62ae8fc2a0ea2bdd7f408d69885c0efb71187b66718a4815b9ba5cb4b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188329490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e840910e9d544a2db734c4f5e91ac0b3683e30d676ff2ae74e0ac9a4ebbd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:09:12 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:09:12 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Apr 2026 00:09:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:09:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1362caa853e87835a06f97724446601f5c6de620cccf2d1b133eaaa541512b`  
		Last Modified: Fri, 24 Apr 2026 00:09:36 GMT  
		Size: 125.4 MB (125377307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:88e4d0dfa2b04ac2931ed098842af181bfca19ce090cce00e12703a3b80db2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2692bbb3dc110595b150a5f737a646410cc2a40602735c08dd2793a0f7e3cb8`

```dockerfile
```

-	Layers:
	-	`sha256:66bbcfccdaed2511e13b10a367006bbc0a10f8c7c5c4d1cb173063d0c840e679`  
		Last Modified: Fri, 24 Apr 2026 00:09:34 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4bcda9249d65a6e84ec9727363fe5f2b79f06ebbbf24b03a1a284d40a713299`  
		Last Modified: Fri, 24 Apr 2026 00:09:33 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:78190154bff3c0a6fd082e101695d74863f4c85815dd95dfd995ad5f7bad8bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132494529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bb9be7881319ab79d6518bfc8808b58d66889de22d839ba7db284f7742034d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:08:25 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:08:25 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Apr 2026 00:08:25 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:08:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb2ae527693de8c13db7615bddf8186492fba775710e9bd07dbe65749190f8`  
		Last Modified: Fri, 24 Apr 2026 00:08:41 GMT  
		Size: 67.7 MB (67695746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ac9e45048066596417be6b34e6d0203300b6ba8ac84ce861b32fbea38d0e86c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d87c061ed2dcffa39d98978eb305d9ff7232c19e0bb93ed2a9bc5965c81562e`

```dockerfile
```

-	Layers:
	-	`sha256:ef0b27d0b7ba22879ab0812937b822560d5e458a3deecf6ee322102bb716690c`  
		Last Modified: Fri, 24 Apr 2026 00:08:40 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b771cf659bc515926ecd267af4cffbdfb291f70cd8587f0165a5a9a272cb2e68`  
		Last Modified: Fri, 24 Apr 2026 00:08:39 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.in-toto+json
