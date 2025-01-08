## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:c04b34451aa4d80f15c79ee0625bbf312dd6c193effcbc11a4b3f8e5e865ac65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d7b2e90f99f058cafb2facf7dd45e4fdc5aed783a51d8485f3dbe0f3b5670cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161909788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce698aec41c656c1f74360d7e27c036c378f99de748eefb6ac8080aef6d918e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09418a4c458298f161b7cb8e02dbabf0f9449aa6cff2494aa0b7513e00003984`  
		Last Modified: Fri, 20 Dec 2024 22:33:01 GMT  
		Size: 99.2 MB (99232349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d1cfefbea0a713dc70f892e115a7f103747fc6a49cddd28cf974c1cc18680ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bf4575eb1d880b7601ab632d091252a06bdf2ca85577b2b9a972b11d16cf4d`

```dockerfile
```

-	Layers:
	-	`sha256:e407eccc4fef41f914790bcc9efce2553b3c704d999e8f18eda6a00e8761a437`  
		Last Modified: Fri, 20 Dec 2024 22:32:59 GMT  
		Size: 5.8 MB (5849558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b12a3d75b3dd70c9e787e0f708a1c265373a6aeafd242d79ec8f07f489bbcd`  
		Last Modified: Fri, 20 Dec 2024 22:32:59 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:515891d12efbc9027d11cd752f4480399ab89888db2d3322819ef9b99c152926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146402360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d613e09ad845eb6a62072b384b7d6ec300c9ec817dd8912b1e28a22cfc2660`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28611e1732f40d2a0a6c310d4b89e8871d66439798ecbb0497ea6d487e8a77d`  
		Last Modified: Wed, 08 Jan 2025 07:28:14 GMT  
		Size: 81.8 MB (81820473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7c6cc5eaa9c8d1e033834a60c999f198818d69a763cbd6f23672ba5d0de36eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b471120d122e809c27c8e4241d1ab9f000ec40575e28bad74b0c213722371c50`

```dockerfile
```

-	Layers:
	-	`sha256:951958db514156c240f34083aa6ffb70d800c1b112e6dc411a1df015a555be36`  
		Last Modified: Sat, 21 Dec 2024 01:47:31 GMT  
		Size: 5.6 MB (5641301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8bdeb017e5f0fe151b73a51c3431cb5d9211c01f4da1298e97600b217d9757b`  
		Last Modified: Sat, 21 Dec 2024 01:47:31 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.in-toto+json
