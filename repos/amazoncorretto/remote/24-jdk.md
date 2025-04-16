## `amazoncorretto:24-jdk`

```console
$ docker pull amazoncorretto@sha256:8d58344cc5ee228271bd825fb525f6af80fbfbc7ba2b914e5493944f6fb87f2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32819409a2997b2f7699566ff7c9a72ebcffc0f20586b4535e909cb2326b0d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243176456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f0bd0e17e8f5d971cded0c925a168707ed6db7cf0b9b177314934549d278ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e5513f0760ee159f76115f9757d5cbf79408cd7da31a5b6c87b0838e791a07`  
		Last Modified: Tue, 15 Apr 2025 23:56:27 GMT  
		Size: 187.3 MB (187269403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:41f65e9a24d4b83c992d38fc82b936de1f5916d9370df63d30d9628473fa45cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5581833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547d99ec2f2a766805876f90ecd6c47f8f2b6304179a5380654a1025092e7f64`

```dockerfile
```

-	Layers:
	-	`sha256:195e4cb50208f94be77e4307e429346a53d536155fada08784cd1b57ef3f3019`  
		Last Modified: Tue, 15 Apr 2025 23:56:22 GMT  
		Size: 5.6 MB (5571595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9748701661df182691cc90fef7783ef581c7290e58cc1b2a1add5d32e433cb`  
		Last Modified: Tue, 15 Apr 2025 23:56:21 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:462b3da0bfe8982910c18dd5e54a3911fc29831d5b604cbc2ee3b60b54aa8b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240274506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acb285ab6a140f23899482ad12e1c78fbdd58adf106d8d35d8471ecaa01813d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:28 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:28 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f2f51d45657c866ea5cda2cc3fc70c3abf42a75618cd6253edfe6d7f5ab764`  
		Last Modified: Wed, 16 Apr 2025 00:21:33 GMT  
		Size: 185.3 MB (185313497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:726fd45cf1b112edf5755157612484eb9a3535aed1636228bbd7a273ee440434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5580916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e527499c16e8d57d7cfe98187fe608612dc775c845cbe54748b4d584a628489b`

```dockerfile
```

-	Layers:
	-	`sha256:c9c1212b37f8de0156a7832079f5b577c0b46604f55d1542cdb92226953551a6`  
		Last Modified: Wed, 16 Apr 2025 00:21:28 GMT  
		Size: 5.6 MB (5570563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653366451f9e2e0cb792364ceb638f0875e38afa596ee7f6b8c5361d0e4159e0`  
		Last Modified: Wed, 16 Apr 2025 00:21:27 GMT  
		Size: 10.4 KB (10353 bytes)  
		MIME: application/vnd.in-toto+json
