## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ffb3b35e6027699389149f98a5b46f0978b1b7c615d9a592c99ec9e73b8fa952
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9c962ef4caee6e211d9bd430f7ca832eb6d413d074c46fde7835557028a8295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134755409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e214e5d7291d37da3abea70a961e37a17eee0dcd674a0b68376c5058cd5b50d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:cb6230c89c15ad3884b7222b06322338ef758165e0b4068d1270a3c8141a3e43`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 52.3 MB (52313926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401132d83f4da46b7c024a0764c60371e0c28520450a327f0cf87625a781ff1`  
		Last Modified: Fri, 02 Aug 2024 14:54:57 GMT  
		Size: 82.4 MB (82441483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da97204dcf017d7a11301fd8902ca4e92e3fe567cf9b3a7c480fe9371381ab91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadbd3b732261f9e657309fb32e82c21d0a3b61319b8ea5ad56aa423d0a98c76`

```dockerfile
```

-	Layers:
	-	`sha256:0c04d4173aee5760d42d50bee4c6322dac0b65400673d3ec7213004c88337f03`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 5.2 MB (5183593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2d9277019e399c44416f075555a06045f8739671973f9ea02c9762900bd071`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3568a880e2e478c3dd6ecb096cc5b0ddfeca65685943b636cc62f2b21941b95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133166360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9659d162d4e298481fd50a5ba300d03e694f2861a7b019842c218b508d4d074`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23586c57526688ba84614d3a31594979480a08758b978e83057d5e0b93611bd7`  
		Last Modified: Fri, 02 Aug 2024 05:46:48 GMT  
		Size: 81.8 MB (81764348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1481c94679768c1044bbf01ac969b0288c7c182da34cb4c69d9200dbb198e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21ae3383a9fbecc7b4bc66dd7b714c204a590c22a3cb951f1afdd4618df679`

```dockerfile
```

-	Layers:
	-	`sha256:049a917c4bcc0373c0a1f8d379ad8de2a6f22e1b620ca68ed66d24df25344ef8`  
		Last Modified: Fri, 02 Aug 2024 05:46:46 GMT  
		Size: 5.2 MB (5182378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f5125acf195f3d1b7b4633142be1b0cebd2e74495367a856cda15b5c5fb04f`  
		Last Modified: Fri, 02 Aug 2024 05:46:46 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json
