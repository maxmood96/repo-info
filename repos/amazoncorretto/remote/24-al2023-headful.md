## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e32d96bee9967dcb52e5656b8cf8e51a4fc1a54a9089917159dee8d5662a9749
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bf5559ce5a826172376591932a038defe37d2d710dbf289b93343c14d866d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156992771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d91451b4dd838afb3884a07f8165d441a32ee7b4bcd66d2ff3356aeab42eb0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771de0c6e09767a08f723a0fd83b85b948176eae9113cd28c7a7bb90621f4a5b`  
		Last Modified: Wed, 13 Aug 2025 23:03:19 GMT  
		Size: 103.2 MB (103154812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82c840b1ab153cfa1d29522abbb373070f480d6c752d93f9f256d126a419afcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30444c069e2c9ceff55d1a2d2247f07735ac90605fbae4c3695ed0921dc86233`

```dockerfile
```

-	Layers:
	-	`sha256:6dd49f9d4d8dfded871d3a4c03e37753224b6f7af20b19828aa199ffc9966026`  
		Last Modified: Thu, 14 Aug 2025 00:49:35 GMT  
		Size: 5.2 MB (5220128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f51c95d36241acf15194dea4993fbe2ada239ab360a20db9cfeae9cadb5315`  
		Last Modified: Thu, 14 Aug 2025 00:49:36 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6cc2e171f72682e38d021c77d12505ca3a96b5865989014f6fa2950f1fa00472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154892956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499837871b2fcb1669b3771c90194d4405b512d3ea81b08457293cdd6f425bdf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effbbe822882d37889404ea1e1c1fe53700ba8cfde4d6559a450d0e123c4697f`  
		Last Modified: Thu, 14 Aug 2025 10:10:51 GMT  
		Size: 102.2 MB (102166562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:10b248fc20284fed58c0b5f91436339781c0977e31e781e57db8fcbd7c2db307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8527a3d52bdd57530c406715f31dc86ea5fd5e43fd8651a7307f5693ec06933`

```dockerfile
```

-	Layers:
	-	`sha256:b71ac7c0747c2b45275f00f436a9ab5073ea7fda1f12a4dc357019a000fe7894`  
		Last Modified: Thu, 14 Aug 2025 12:48:23 GMT  
		Size: 5.2 MB (5218942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3379143d5cf03257085b679358951d811ab23d0adae4d6b0e793e92a1fd8ae`  
		Last Modified: Thu, 14 Aug 2025 12:48:24 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.in-toto+json
