## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:dabf238ae27acc958d01ccfd9ce38a14fbeef7c3d7523c980de6334c0a0afc81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:97276b7786a4bfcb99f24636a5cb7b0dbc8abdd20c55ab3ffa9dbad08ec8df4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188179867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a72ee6ae533b860d1526d0a84f4bc7d12bc5bba662960a4d622dca8009b9495`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=1.8.0_462.b08-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f72842542f7f86448eb2de4b88f948f1751f5189fe8ae412b9b38cb34a64f2`  
		Last Modified: Thu, 25 Sep 2025 02:16:13 GMT  
		Size: 125.2 MB (125246026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c560bdf41354614fe4c1f0b101f64cf8792e989df5e3bb37a4c1e35579898fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae67a689c698f5d603efba6e2eb04cb61b17bbf020ab4de6e7b6d0ccbadfe66`

```dockerfile
```

-	Layers:
	-	`sha256:8c3d5ea5a52d470697b1ff45c9dc7e235a698fb7f60d11676f99a2eabb069163`  
		Last Modified: Thu, 25 Sep 2025 03:52:47 GMT  
		Size: 8.0 MB (7977414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60a200e8ee205c29ab4817880fbd1a344e8e90afc421c2dfe496c4855bab0a7f`  
		Last Modified: Thu, 25 Sep 2025 03:52:48 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f23306c8b9ecdfb18293a3fcf5ff978628850aa189710a691d86eb130034812c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132346616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ea3fc20aba5242aca2fd9c55a3886b6388b36fb03f286d2cc7146d8957f53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=1.8.0_462.b08-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa79339eb5e7edd8c40684caf09bb207bb03f10acb467f3b70ddc745a276928c`  
		Last Modified: Fri, 26 Sep 2025 01:13:25 GMT  
		Size: 67.6 MB (67553469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a077fdcb1993ecf9e6bc78ae8dfdb02271a39bbe779d8aefdc920570c2bd755d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8030d00dd8c1169fe86e58d2be14e371ca8b6ce885baa0a01f320574ee7a1e`

```dockerfile
```

-	Layers:
	-	`sha256:0e546858487da13df22c7e54f9c5245fbfd125550db4709bbe74ad4eb2b4344e`  
		Last Modified: Thu, 25 Sep 2025 03:52:58 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73d39fedbc20462641358d84a102762fd5f1b3b2b4ba75af310f5f0c23caf12`  
		Last Modified: Thu, 25 Sep 2025 03:53:00 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
