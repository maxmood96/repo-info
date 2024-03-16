## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:82510c569c0663be837b7d8cb0c55b115c7b583535f5d8ca9de2ce228218e603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:66828d832d23cf929fd337de945944e3dee5dd9784fcbc9995c02513f72ba162
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141861114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f0f7f8065aaf740d1fc0d16e9db445bfb398d1c684dbbf690906c5b0382e3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:11 GMT
COPY dir:d7da6e069b79aa8b51b20a889b996a9bea020932e2948f46e1e355ca42d78f77 in / 
# Mon, 11 Mar 2024 23:50:12 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 02:58:24 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 02:58:24 GMT
ARG package_version=1
# Sat, 16 Mar 2024 02:59:11 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 02:59:11 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:59:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:89b8a841604356b93248cef633e19448985a8a9e86277f3b31c2e3860eabe2ad`  
		Last Modified: Wed, 06 Mar 2024 01:18:19 GMT  
		Size: 52.3 MB (52337114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f898ac5fce9524da9adef4af428bd104f28ac7fb73c3f362be482e95e5f40a`  
		Last Modified: Sat, 16 Mar 2024 03:15:47 GMT  
		Size: 89.5 MB (89524000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ee65bcd50cb2758853b06d3f74c27342db8b99dfeede24c0a06b1555dc98ec44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139998244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486deaee32b104f1f8ca8e3e000d063d2ee7ece5e12706bdab89cc76385701d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:46:56 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 03:46:56 GMT
ARG package_version=1
# Sat, 16 Mar 2024 03:47:38 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 03:47:39 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:47:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b87f1e504d0df5a8af6e3c84b3007fe76194a1c3cbf533e4546c56fd11e073`  
		Last Modified: Sat, 16 Mar 2024 04:01:39 GMT  
		Size: 88.6 MB (88583658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
