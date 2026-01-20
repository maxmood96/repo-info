## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6c4124155ef86659fc927e1cdd396c3bb9823ce70b0ffcf6092705b08ff77bb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:27f4c73fe03749f0220ba8a1b75b60974951a8c1ec11c3911e07e4ecbbba3e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143983274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a99f1c8137f47560c5e924b572cf7474965c81db9bdd5acac150598e86e5829`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:09 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:10:09 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:09 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:09 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d35105ef888879ed7ff09c1799d3deea54b1384ea8d21eeb5c6604ceab08f8d`  
		Last Modified: Thu, 15 Jan 2026 22:10:49 GMT  
		Size: 90.0 MB (89962070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e228f4e070c63a75249dbacdc4465af01c10caca6de5a20d45ebfe4cd0209cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205c84cfcfa3ad55cb1f6466c853927bc150001e0cbd0c1ad68ae6f3ba7dbfee`

```dockerfile
```

-	Layers:
	-	`sha256:c89bf6ee1d92d13231a470819b8593c8ee905fa772d361e895195ef73b2ea883`  
		Last Modified: Thu, 15 Jan 2026 22:51:02 GMT  
		Size: 5.2 MB (5209947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53a2a47e6a0feffae68492f725e8cc3c12a765378ce1f3c065e2099f88613d6`  
		Last Modified: Thu, 15 Jan 2026 22:51:03 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9a1645abb5eeda64c34efcbb2be32402a2a6d497dd5b9ca28648bcf8397eda23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142012184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa1e38965e2c0160db53c6f3da0cbdaec908617a74e5f3ecd69f6b3d32a8252`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:11 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:10:11 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:11 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:11 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccceb3c693116c4616e3e7fbc63585c535b85e722382409decb6c621c87e994`  
		Last Modified: Thu, 15 Jan 2026 22:10:44 GMT  
		Size: 89.1 MB (89097827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:10b428b3e1015458c729cc5d989011a8e0d00834ac7b621a34086f35c6e8e7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892d172e8cea7872e35091bf2ccb1d33dd6a267aa42bfc69e0e681aefa2837a3`

```dockerfile
```

-	Layers:
	-	`sha256:da98df605423087103cdc2d6837ae7f7e539874f7b9c28cbf388d509b4d5f6dc`  
		Last Modified: Thu, 15 Jan 2026 22:51:09 GMT  
		Size: 5.2 MB (5208740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3d8826cf0e689959a3b083bef0df66b3725c31f84e7527d820c2e8af0d485b`  
		Last Modified: Thu, 15 Jan 2026 22:51:10 GMT  
		Size: 9.0 KB (8969 bytes)  
		MIME: application/vnd.in-toto+json
