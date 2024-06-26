## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4783dd01f328b900ba0ccc4579ee4fb91ba5e55a72275ee93cccbd8e8803ca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1f72d315f8044eb097bc925e392f3f19a17e0bb941352ebc2214f8d09172addd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141881744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1495098183b27925232f8c84a46d19644ae02c38829fdb7c2d05cecb784d22ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:08 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Thu, 20 Jun 2024 17:20:09 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:51:53 GMT
ARG version=21.0.3.9-1
# Thu, 20 Jun 2024 17:51:53 GMT
ARG package_version=1
# Thu, 20 Jun 2024 17:52:40 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:52:40 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:52:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c8f1d7c694c6b94c0ee687a44a28334fa5bb4628f7d79fb79ca34627cd4a0f`  
		Last Modified: Thu, 20 Jun 2024 18:24:50 GMT  
		Size: 89.6 MB (89562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f0ae0434f34d1692ab9e9ef1467990ce82e011ab176e0a2462f9ced8c7a7ad26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139994771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4d8a3d864a2f8b09ba0d413cda235aab11cc3c4914f89a7b20ad4a7e6bc08e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:29 GMT
COPY dir:0c9326c957c0b22895e223bbba2686fb8615da2af32396db3026daf720546255 in / 
# Thu, 20 Jun 2024 17:39:30 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:27:41 GMT
ARG version=21.0.3.9-1
# Thu, 20 Jun 2024 18:27:41 GMT
ARG package_version=1
# Thu, 20 Jun 2024 18:28:24 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 18:28:25 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:28:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:15e2a4581bb8a27d0865d7375063b10dc543dbcfa6a288911a297aaf754984d9`  
		Last Modified: Tue, 11 Jun 2024 02:05:34 GMT  
		Size: 51.4 MB (51406731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf51887df88ccfaf2ad769497e28e80d5ac730b9e5def46fd0080f042fe7947`  
		Last Modified: Wed, 26 Jun 2024 16:53:33 GMT  
		Size: 88.6 MB (88588040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
