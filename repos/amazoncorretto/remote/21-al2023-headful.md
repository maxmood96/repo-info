## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ef7c9b4fc00482c452d9dbb958221d3ee7fdb79398e3df02d604b3f4e9b8531c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e0d9293f1f9387c1a1c7eb0eb90c5bdb6701c64ce404d7705dec708850b26047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141973457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2531be504461f58f540c01bca18b0adabe43417756cf67cb86bb56f3a783bda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caba7b0b101b6f0ba33b2a048242f79d103d0c7415cfc59e606484c8db01cc58`  
		Last Modified: Mon, 21 Oct 2024 18:57:09 GMT  
		Size: 89.6 MB (89629625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7717826a91b8f22dba21d9cc8a1b74c5eb8fd103640d0dde9cbcae5b7df3b21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cd2ab4bfbb9d1ed9cfdf1fc1543f1477ce3712d4a9ad4ab9ae5d835607bf36`

```dockerfile
```

-	Layers:
	-	`sha256:d44e450a1d299250081e52cbd4bdbcf367de6c14ae8562bbd29bbd69593596db`  
		Last Modified: Mon, 21 Oct 2024 18:57:07 GMT  
		Size: 5.2 MB (5211479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37ef037a39e4d153afa5145892b7abd20d98cce382c577ca6971e0a094d3b90`  
		Last Modified: Mon, 21 Oct 2024 18:57:07 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9129ceaf785daaf38d702d2718ed411176ba6ee00215876acb26898f51c5fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140111891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ae763167238ba0e7b5a0a9b5e7beef8ae3124c60aa1999aaee0bebc9d331fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297b35094500b1ca957c3beedbc5298d8fae9f28d9dccb57ec00db2996d4d7b1`  
		Last Modified: Wed, 16 Oct 2024 18:35:38 GMT  
		Size: 88.7 MB (88685527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ec7e60eb66458bf56fc2b69982946b2d2507e13d9847acfad2d77ed1eab22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a789943ce515013833c50740ee009186c7566908a0a967ded332e6a59c47bdc3`

```dockerfile
```

-	Layers:
	-	`sha256:3403ab3ea17aeb3f4008f0416cfbb6401bf815a81ff4faf55653c39f35867dce`  
		Last Modified: Wed, 16 Oct 2024 18:35:36 GMT  
		Size: 5.2 MB (5210100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2abd94bdd07678524d2cc111efbe9c799dabf9e5045c690d33e352fb84a502`  
		Last Modified: Wed, 16 Oct 2024 18:35:35 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.in-toto+json
