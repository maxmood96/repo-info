## `amazoncorretto:25-jdk`

```console
$ docker pull amazoncorretto@sha256:ab78a0105e5bbb25cdd16b438e17581788d91883670d37d02bc72139e0f4a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0bd78373cd452ca15530e4c57a26506ce612886d9ce36735efa57236642b34e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243214994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744e9c91fd527d74bf7ebf1b908744910f606c7c9c01260b6365da216678679d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:36 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:13:36 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:13:36 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:13:36 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9307319cf5c73e99e04dcd81f4b9092ff8c453a217e95ba5b67ed0628f3138`  
		Last Modified: Tue, 27 Jan 2026 22:14:01 GMT  
		Size: 189.2 MB (189191158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2e0f9969cf90939c1e7338710648188c7a8a4a02ea1fc18fc575b8790ef8e1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5340089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4449ba79cdbe1ea6f04a19ffaadca1b5466faeb11fd2f9e26863992ed7a7bc15`

```dockerfile
```

-	Layers:
	-	`sha256:52b2a870ed384c1e6e7962baf706462bee2243347aec34c1c9524811aac93876`  
		Last Modified: Tue, 27 Jan 2026 22:13:57 GMT  
		Size: 5.3 MB (5329580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d9c59cf2493a5a84053893ca5704e30f82d1fbe04279e3524d85844825778b`  
		Last Modified: Tue, 27 Jan 2026 22:13:57 GMT  
		Size: 10.5 KB (10509 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7ea67371f9d22ee0413934006476ebc78ab83d7a5288331599cb5b548076b078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240007816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d1cf89c548ed8518d2449290b4608a73d938caf241aea2eac68f2b44358a45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:56 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:12:56 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:56 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:56 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af45d8028ea21d913fa4bbb3381bedf24377df2182daab5e8ed011f7165bbfd`  
		Last Modified: Tue, 27 Jan 2026 22:13:21 GMT  
		Size: 187.1 MB (187091178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fcd3a6f884fc6f5f493cb86cca60299d846d81dbd12785aa8242a4ba2535502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8ea416fbfddc75d7c97df7919da095265cd7bb5a9518a169b0cb32c4bf6bb`

```dockerfile
```

-	Layers:
	-	`sha256:0dd96a112f52a080e4b15830be439add4e265a701668ccd91624b2284ee9b2e5`  
		Last Modified: Tue, 27 Jan 2026 22:13:17 GMT  
		Size: 5.3 MB (5328560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9aab048ca48067ba1e1da0b063d89ac64a9c0299eceb7bf2ff4a89cafbc5b4`  
		Last Modified: Tue, 27 Jan 2026 22:13:17 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.in-toto+json
