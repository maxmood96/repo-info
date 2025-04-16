## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:54ca7cdce16d006aa1cb71ab9b34f47bf359241c0878cd20f3bd51947fb0874b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e4b036329a90f36178f3cb2044eab71da429a94166f3403433f99f287a9b4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228260146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef411722571c47c234da192bfb65493454d2677e6c57a5753bbb0b07aaf9a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76d174baa4b4e75f9eb0a2f4e0a2d0e852742d7ec4549f64e4ce74620907306`  
		Last Modified: Tue, 15 Apr 2025 23:56:12 GMT  
		Size: 165.5 MB (165507257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:94b5835824c1a3a20d75e5e912a5f19c85f8adaee44e77145046ad100e691495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f9df9d1f068700e54832c9cbb06679b18a6ae66c72ffab6b7c1b0a9bab8080`

```dockerfile
```

-	Layers:
	-	`sha256:ba924909a44ce4d5f0fd50a10501b5cd6db7e49da4c5b5ead10f231753fd9084`  
		Last Modified: Tue, 15 Apr 2025 23:56:09 GMT  
		Size: 6.0 MB (5955224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ee07f8bd4890c06c5f9a5ac8919fa4c0d673a7cc19d48a08a9f61fbf2bedddb`  
		Last Modified: Tue, 15 Apr 2025 23:56:09 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5d61e84ab0bd12343c502bd21f3f0d64504b31e2bd577ad7e41929f3cd78661c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220526449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da546b83d75b4fa45f63f584974dac4ca17b2c6e805366b7b8ba5b2af789dda2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272a6b17e0b8de14bd82fc14d7ebc496de175a96cd527efe4405720a878ce0b1`  
		Last Modified: Fri, 28 Mar 2025 00:18:43 GMT  
		Size: 156.0 MB (155960627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:236962a0ea5f95498d4d8317239e374ed5a98914c2a7cee391a95d8c705e334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ddf096b585501ab721c359a97b52455f65189324fb07e546c091d6266756b5`

```dockerfile
```

-	Layers:
	-	`sha256:5fac89a5336420e76264da0eb6f2b1b4575d81d4b8cace02a084efb31a69d6cf`  
		Last Modified: Fri, 28 Mar 2025 00:18:39 GMT  
		Size: 5.7 MB (5747064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746eac4559a2023a6b638b7235220bcc2d60cf3cc4f51a80bed6d20be5266a88`  
		Last Modified: Fri, 28 Mar 2025 00:18:38 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json
