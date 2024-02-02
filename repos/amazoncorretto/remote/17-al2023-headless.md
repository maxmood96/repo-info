## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:169c2472e61d29a24d502368a7f31d3f903446ea10e1884578beb73b57ecb60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2848d9855d52f7b169bd37f568298ef1c9a04927e749937137c5497735bb2ce2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134578210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20eb0e5dfb4114635313dcc39b345c74f7f196902cabf78b69d192a67425630`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Feb 2024 23:53:41 GMT
COPY dir:a483dadf03df21b4c46ae05c4564496c155a45055f49c3293b4e7554c8160845 in / 
# Thu, 01 Feb 2024 23:53:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:42:01 GMT
ARG version=17.0.10.7-1
# Fri, 02 Feb 2024 00:42:02 GMT
ARG package_version=1
# Fri, 02 Feb 2024 00:42:42 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 02 Feb 2024 00:42:42 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:42:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:567d8ee5457ce911a8659b74a8187fbe402d4417070b8c4af0bf7d6289c1baae`  
		Last Modified: Thu, 01 Feb 2024 00:30:11 GMT  
		Size: 52.2 MB (52245559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca18e15c45da3230f51a9e013cec711d414f620e68a6355c356b9be73a07f407`  
		Last Modified: Fri, 02 Feb 2024 00:53:45 GMT  
		Size: 82.3 MB (82332651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dceab65d6e1a7e6522e5e4c71d2cc18951a348483c413cb9ccfb89c617c6a730
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132990563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c337aef3da9c0c1592e727ddd3b8c4bd0590135cc5d1a5c1c5b641b41c332c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:30 GMT
COPY dir:da17a174bd602e575391d08ca94d5595606a8d6d7b3b957cdec78f5fad499e19 in / 
# Thu, 01 Feb 2024 23:30:31 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:52:07 GMT
ARG version=17.0.10.7-1
# Thu, 01 Feb 2024 23:52:07 GMT
ARG package_version=1
# Thu, 01 Feb 2024 23:52:44 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 01 Feb 2024 23:52:45 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:52:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d111cbc02b249a552b77e87298e3df2ce29173bc39b7d82aecba5ca8a2ab06d2`  
		Last Modified: Thu, 01 Feb 2024 00:30:08 GMT  
		Size: 51.3 MB (51322438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfc8cfef678e4cf9488d3842e7d35838ffff84e1701eebe5d4931e7ff425266`  
		Last Modified: Fri, 02 Feb 2024 00:02:18 GMT  
		Size: 81.7 MB (81668125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
