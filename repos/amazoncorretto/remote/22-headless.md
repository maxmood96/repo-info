## `amazoncorretto:22-headless`

```console
$ docker pull amazoncorretto@sha256:4e66746f6b84fa5fb8166a08de45e0ffd3dff429644971888b35f1bad9ed7df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e0957290cef4f6d961d3fc82da9160c73701f9ed1329a30f2e9ee107b10128f2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140918677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a5981632f11f4405e84dae42f73273c635948f4aa6f91302d445f3870b29b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:08 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Thu, 20 Jun 2024 17:20:09 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:53:17 GMT
ARG version=22.0.1.8-1
# Thu, 20 Jun 2024 17:53:18 GMT
ARG package_version=1
# Thu, 20 Jun 2024 17:54:16 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:54:16 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:54:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7784953d21226227fa19226bd07e81fc609a07c867f4989cf4da685fc92fff`  
		Last Modified: Thu, 20 Jun 2024 18:26:00 GMT  
		Size: 88.6 MB (88599164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6c263c1d51590d9fdc8224c8e8633a4e405b432a362ad3ce3bd4ff97fa21452a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138956671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c559022856ba08e93f49995e00aefdb99c6a930f811a90a778ebb6b309bdef4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:37:36 GMT
ARG version=22.0.1.8-1
# Wed, 05 Jun 2024 02:37:37 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:38:25 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:38:26 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:38:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269afa861639601479efc5a1ed8a54eabd15bfdc1969d4003faebe112ee7429e`  
		Last Modified: Wed, 05 Jun 2024 02:47:46 GMT  
		Size: 87.6 MB (87552793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
