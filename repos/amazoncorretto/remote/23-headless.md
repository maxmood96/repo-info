## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:3f584a7fc84b7a32775de635662513b7ca5a6c7e271b7647708713b2b22de7ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae078fdec7ed37db60b4a749e681bd40d67ce800eb08aa9af528dab5362ace9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146266622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77e3b5f3b6abc5afa0fc13dda0914167831cef35a9e5b34f2147e5105e45b2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990892632b29d2bdc025aa0dd71a6801906843d6914cd0d0907e1c737f6957c`  
		Last Modified: Thu, 13 Mar 2025 22:53:10 GMT  
		Size: 93.1 MB (93139746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ca1297bfc64714c7f1dfaa7ba7ccf602ea3783bef17f3f1c9a061043ebecef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a284ebfdfd047a8a9e9de3ad879edc6e3e894fc5a10aa197582e2a3be242176`

```dockerfile
```

-	Layers:
	-	`sha256:b5e8c929d2537e56c0650d7c55bcc640c2114321922776c517cf9f220beed70e`  
		Last Modified: Thu, 13 Mar 2025 22:53:09 GMT  
		Size: 5.2 MB (5164154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a94f86c8e07f10a929669a5025bd565ce80cf2a136f545139128bb991a79075`  
		Last Modified: Thu, 13 Mar 2025 22:53:08 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9b4d6defd25122542c2f9da44a59c7247a1e1384bf110e31808fe325d4c1844d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144421878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f024c23a1ab8ba45e33c045d19e153b726fb29bdc4b89e0fffea3e080194ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c195d46c6ce9b8286774b6e1c918bef977d4403611e7a1560778cadf49b6cd4`  
		Last Modified: Thu, 27 Feb 2025 21:25:40 GMT  
		Size: 92.2 MB (92150608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:695158729f707d581e56c8953e46e4442aa4a294726f0879d3e5c9f9e7a77e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648d805845e204921e58c12211c1bd77a90a98ebeb1aaa2b66a17cfdd6e13b46`

```dockerfile
```

-	Layers:
	-	`sha256:c75f0461462f4cd77dc02a6485e57eea9356c68e4b9eb227fe9d20ddd546f873`  
		Last Modified: Thu, 27 Feb 2025 21:25:38 GMT  
		Size: 5.2 MB (5162143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724a9537474092d93b5aff502be9bebeac183ae8d91ca6a8770eec0e2d945b25`  
		Last Modified: Thu, 27 Feb 2025 21:25:37 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json
