## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:869ab4083da3414584f3f9236741bf40c62d44f133b93c19487782c09773700c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:03e96648c6439d6e91a65c919d241645cbfea0c677bc716a1dcb628a90a7b745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134817938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67a564969ba9e8b47a94dd8894b6bceeda604fa7b5a17daf8b786a20b81d12f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:08 GMT
COPY dir:acd83a6b32519bdad84d6a4d016402a3bfbd7ec8056e92d01a2222fd4cc63d9d in / 
# Wed, 26 Jul 2023 19:20:08 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:19:26 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:19:26 GMT
ARG package_version=1
# Wed, 26 Jul 2023 20:20:04 GMT
# ARGS: package_version=1 version=17.0.8.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 26 Jul 2023 20:20:05 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:20:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0ccf2bf65eb109135ce4e32ed827c8fd4df1396c406122da0b40d4fd7f088839`  
		Last Modified: Thu, 20 Jul 2023 17:41:27 GMT  
		Size: 52.3 MB (52310872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca36bf9cc2bf13d3ab5f856a178bf2445ec047056aa3b779738191113d920344`  
		Last Modified: Wed, 26 Jul 2023 20:30:26 GMT  
		Size: 82.5 MB (82507066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f92ca99d51d4f114a48f57e2a493b297f41695b1a0aadd96e7f12e1b90bdf304
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133177556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ca5f21974c5d52ddd833e644bcc0d93704387f0c4f4f60e22ca7a578257dca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:44 GMT
COPY dir:ab5df2603dbae327b5eecbb1ba196f5a1f17cd096f7248968ddb73809ff1f45c in / 
# Wed, 26 Jul 2023 19:39:44 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:21:53 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:21:53 GMT
ARG package_version=1
# Wed, 26 Jul 2023 20:22:25 GMT
# ARGS: package_version=1 version=17.0.8.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 26 Jul 2023 20:22:26 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:22:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:91b7fefd504f27afc9eac17100f8e7fa41446c3fdfe003e74025c20a9adb95f3`  
		Last Modified: Fri, 21 Jul 2023 03:06:49 GMT  
		Size: 51.3 MB (51349707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cd005374bf8269f13c3c30a33211fe170458e1ed84be726eb84308f801cd1a`  
		Last Modified: Wed, 26 Jul 2023 20:30:44 GMT  
		Size: 81.8 MB (81827849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
