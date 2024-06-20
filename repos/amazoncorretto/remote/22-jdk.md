## `amazoncorretto:22-jdk`

```console
$ docker pull amazoncorretto@sha256:a93fff924351e92140e46f07c41f8739b436484de5b45b3b42c5daf64e4c22e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55f8b6423fe72eef99a4769aeff049301a787b450f6888505511475888f1259b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221175258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1249f70e25ba31d503cf21c073ab47ef4b1e8a936f8194c6833ea33a12232`
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
# Thu, 20 Jun 2024 17:53:49 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:53:49 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:53:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79af680dc4fc4d7e2a1ff0b53d2a8ae13a9db622c46f5bcbdf87b037f1cc44eb`  
		Last Modified: Thu, 20 Jun 2024 18:25:37 GMT  
		Size: 168.9 MB (168855745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1b242d4287aff125ed40598f641dcb669a5191420807d173faa2b2fe748c5c58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218269341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21914eab03c11c328c9315efd6d8cc4e3ba773d1f73629c2bf0ba6f6d0a28f`
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
# Wed, 05 Jun 2024 02:38:01 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:38:03 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:38:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5192938b316e73cc42b07ca34a5f09ace280226bf23b3e93101283c7c7c5953`  
		Last Modified: Wed, 05 Jun 2024 02:47:25 GMT  
		Size: 166.9 MB (166865463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
