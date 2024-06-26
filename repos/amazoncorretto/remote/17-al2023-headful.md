## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:1311b726001db7b9330443336efefba97056c3ec2a1ee5ed6b8f7dd5deac5691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55d9a7c78a989f41d86241fdbe6ef820bcd6a1f02590f907fc96a5d6de43aded
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135424991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab0dcb36a641800de82e151fa7fe2da0c2265464f4822f69e02c0605e8608b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:08 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Thu, 20 Jun 2024 17:20:09 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:47:51 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 17:47:51 GMT
ARG package_version=1
# Thu, 20 Jun 2024 17:48:58 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:48:58 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:48:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecec290eb176178e5a05d15526d011881744ec778c00663fb9fe8e62cfb3685b`  
		Last Modified: Thu, 20 Jun 2024 18:22:27 GMT  
		Size: 83.1 MB (83105478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:68ad7c182c96bf43ac2232a7e1ff5dc33f77257b38803c66212c82def2dfe70b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133843119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f93e01ff4c6ad840ef548d44b3efebbc266b9c023f7a287954285d3a0f0737b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:29 GMT
COPY dir:0c9326c957c0b22895e223bbba2686fb8615da2af32396db3026daf720546255 in / 
# Thu, 20 Jun 2024 17:39:30 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:24:05 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 18:24:05 GMT
ARG package_version=1
# Thu, 20 Jun 2024 18:25:03 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 18:25:04 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:25:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:15e2a4581bb8a27d0865d7375063b10dc543dbcfa6a288911a297aaf754984d9`  
		Last Modified: Tue, 11 Jun 2024 02:05:34 GMT  
		Size: 51.4 MB (51406731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0609835fe7443e7341216f87aa356cf149056c79232dfad717b43dccdc638511`  
		Last Modified: Wed, 26 Jun 2024 16:50:20 GMT  
		Size: 82.4 MB (82436388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
