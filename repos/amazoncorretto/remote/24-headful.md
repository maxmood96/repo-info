## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:550529d74fdecd2574c5bb79f6ecd9be7ce93e79f14881f9e34f996f802c95d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:41dc24f6c74abce6dedd6eef82dc511ddd2c8224261de1c1b590aea8732048bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158976262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c7d06f615a1bd90906826e7397ff065f46961071d64956b4ba6f5f72af11ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1900cee18e153b0e8ee973626cbc1c94d2c48cd15b0ed203e2307e46ed92693`  
		Last Modified: Tue, 15 Apr 2025 23:56:18 GMT  
		Size: 103.1 MB (103069209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:49ca9074b8a69edf0ba067fc22b2fbd4a184aadeb96d90155ad797c1a87e2865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03243a3e4a7dadd0e3853774deb33c3a1e98b054f339d6e919c600cfa2eb296`

```dockerfile
```

-	Layers:
	-	`sha256:5d220821af41a8a8eb8db967eccd9f25f0ab9991bc78044a46826a81841e3f37`  
		Last Modified: Tue, 15 Apr 2025 23:56:16 GMT  
		Size: 5.5 MB (5462905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ff85ec0bbcc01a97e7233d238b73359f67658e60d1bac00e515cfea8a97c17`  
		Last Modified: Tue, 15 Apr 2025 23:56:16 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:962b56c62125914170b7fbcb22eb03141a97032f317722aa3809e25d2d6f3aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157041989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b1de68ea0ac42b282fc571068b3faa2db49a0e59f797c66440fc723179b82d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a1b3f4fe85199457c7a794de97ab6cb51bc5606e8de9e7d9a240a7f417d9c`  
		Last Modified: Wed, 02 Apr 2025 00:39:50 GMT  
		Size: 102.1 MB (102080980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6ee9f121ec032d7244f4c4658dfafed55bf78f7c52ab19be83c5c44b87a1903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254ec97e5dfea269351bcc84c7048b9d142afa39b41e9defbbf3ed5c3b45abd6`

```dockerfile
```

-	Layers:
	-	`sha256:0ccc73b45c504d6bab902a5be401344ed66aab74f1cc75aa8c7c201e2352097b`  
		Last Modified: Wed, 02 Apr 2025 00:39:47 GMT  
		Size: 5.5 MB (5461717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe09f3f811b22e9050a66f55ff97ef97f756e923f76f77eeeb0831101dbcc86`  
		Last Modified: Wed, 02 Apr 2025 00:39:46 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.in-toto+json
