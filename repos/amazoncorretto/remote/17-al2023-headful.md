## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5e1a77dcb32e0f53f8bc765e84818ce30c42693d90ec3b4e3e2fedb06735909e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7bc43ab36968e75f78ffafb0ffb4e900aab147f1ce418da3784072277d59731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135224558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2bf8ac068de498720505e59d4aadaa962028664557d857c77d0ab02d0e2b09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:15:24 GMT
ARG version=17.0.10.7-1
# Mon, 26 Feb 2024 23:15:24 GMT
ARG package_version=1
# Mon, 26 Feb 2024 23:16:36 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:16:37 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:16:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d2576641e3136b73cb29a4f03569ea95a7e749e41f5b5453cc05e5c44682a3`  
		Last Modified: Mon, 26 Feb 2024 23:28:30 GMT  
		Size: 83.0 MB (83014379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:72598a838d1c497f98aa39d4830b3276b2489c1f14406646d3a68f3938bc7bce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133773434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28aeb7f274da97bd9c465b6dcf1dffbb9e765a00b497f88f6ff14dcc0b8a7824`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:43 GMT
COPY dir:2bac3e0f2f9808be2259a0eea507562cc31d6f7cf5f26809139e8bb63fb6b535 in / 
# Mon, 11 Mar 2024 22:39:44 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:14:50 GMT
ARG version=17.0.10.7-1
# Mon, 11 Mar 2024 23:14:50 GMT
ARG package_version=1
# Mon, 11 Mar 2024 23:15:44 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 11 Mar 2024 23:15:45 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:15:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:89bff426afee4c835c6855932ea2864aef333271964dcfe8c4e0cd4be90649f8`  
		Last Modified: Wed, 06 Mar 2024 01:18:22 GMT  
		Size: 51.4 MB (51406909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec32011f36a9007c805bb203d3743fdcfa2ffad501b70da737e82223cf84129`  
		Last Modified: Mon, 11 Mar 2024 23:24:57 GMT  
		Size: 82.4 MB (82366525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
