## `amazoncorretto:11-al2023-RC-headless`

```console
$ docker pull amazoncorretto@sha256:7f075033436849e94c2ca8000cf067ec81bce61b537ef6a70da66202f0dd9f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-RC-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5ca6803c441721268681013e283756411c3cdea4478416a9b6080255682c8603
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126277782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f623be3048e47bcb78772975549dfedc292752bb255b1bd71eb5c7fedc234da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Mar 2023 23:39:28 GMT
COPY dir:6216321324f425942c20403c2b329b848d15da8e81fc7ff80ef8243170c71d61 in / 
# Wed, 15 Mar 2023 23:39:29 GMT
CMD ["/bin/bash"]
# Fri, 24 Mar 2023 22:45:00 GMT
ARG version=11.0.18.10-1
# Fri, 24 Mar 2023 22:45:28 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 24 Mar 2023 22:45:29 GMT
ENV LANG=C.UTF-8
# Fri, 24 Mar 2023 22:45:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7ec7ca6df11f626205137bf1acf9efe68492ded671bc9f023577533727044ff6`  
		Last Modified: Wed, 15 Mar 2023 23:39:46 GMT  
		Size: 51.3 MB (51302659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3dcb16c191c645983ff9544ebd736d1047bbdcf6a0da047574976dbbefd481`  
		Last Modified: Fri, 24 Mar 2023 22:47:52 GMT  
		Size: 75.0 MB (74975123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
