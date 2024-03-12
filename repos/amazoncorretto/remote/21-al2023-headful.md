## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:129e67a961bde13b330d18bc095471b0391b0916ac6bc73ac7ff18b2946e8713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:283c5f7a015b64095739e4cc47f371435e60b44d4f8463fb8be186fa8539c3e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c517448faf9eb0f3147e0fe65336b3098929cb514568bcf68c957829bda9af1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 20:53:30 GMT
ARG version=21.0.2.14-1
# Tue, 27 Feb 2024 20:53:30 GMT
ARG package_version=1
# Tue, 27 Feb 2024 20:54:36 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Tue, 27 Feb 2024 20:54:37 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 20:54:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dac5bfc4eee132018f43dccf9e112ea96d4f2dfebbedb7dc8324305184444d`  
		Last Modified: Tue, 27 Feb 2024 20:58:38 GMT  
		Size: 90.2 MB (90216358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ed938d22f7c4dec9463b198fa25f52e28a77e79c05f334845c50dfbec2ecba2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140709601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc1486b79c36cf90229459ee9c721bfacbca3ef32029aa988b2fc116d9e4bb7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:43 GMT
COPY dir:2bac3e0f2f9808be2259a0eea507562cc31d6f7cf5f26809139e8bb63fb6b535 in / 
# Mon, 11 Mar 2024 22:39:44 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:18:05 GMT
ARG version=21.0.2.14-1
# Mon, 11 Mar 2024 23:18:05 GMT
ARG package_version=1
# Mon, 11 Mar 2024 23:19:02 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 11 Mar 2024 23:19:03 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:19:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:89bff426afee4c835c6855932ea2864aef333271964dcfe8c4e0cd4be90649f8`  
		Last Modified: Wed, 06 Mar 2024 01:18:22 GMT  
		Size: 51.4 MB (51406909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359054530dc72df8ae136bc54509b8da885f519141ad8e8bde4a61dd2948d75b`  
		Last Modified: Mon, 11 Mar 2024 23:27:18 GMT  
		Size: 89.3 MB (89302692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
