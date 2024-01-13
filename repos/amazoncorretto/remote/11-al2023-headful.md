## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:30b686c460f62205283bd4d30403ef4eadd8fc85ecddb4365250bcd4bac19fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f124c8bad96b57335dcbb5dab82b04a6c20439406dcbac9e9614ec17aa1b1167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128990057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acdf034a492783b0e51e1ca03d9eea24f8b7132b9a376bc0794d91a859b8bf1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:33 GMT
COPY dir:3d1c4d9e1017e7de559aec6b3779bdf6668d0e4f73f6af00952a84abd805da43 in / 
# Fri, 12 Jan 2024 21:45:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:18:00 GMT
ARG version=11.0.21.9-1
# Fri, 12 Jan 2024 22:19:05 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 12 Jan 2024 22:19:06 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:19:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592fcbe9ebcec6e31ad10b3d219e4f61ce8e39180e215fab37ae75bc7ac4c0b7`  
		Last Modified: Tue, 09 Jan 2024 00:19:51 GMT  
		Size: 52.2 MB (52238109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a183236e7cfeaf2f2afdbe7e14372112e9cf62db3636739ab80dc23eeb65358b`  
		Last Modified: Fri, 12 Jan 2024 22:30:55 GMT  
		Size: 76.8 MB (76751948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:07e8b434df6a502b44c8a1340287d33ede64d072e4b50082f779f702ebdccfc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127226039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf22968642386b5f1464d8bc280a4a3315344bf5a380077d2f96eaea8152267d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:07 GMT
COPY dir:80de4926459dcf07edafbe2044439672e4fed6bf5796881b9953e9ffab3571d8 in / 
# Fri, 12 Jan 2024 21:49:08 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:31:29 GMT
ARG version=11.0.21.9-1
# Fri, 12 Jan 2024 22:32:22 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 12 Jan 2024 22:32:22 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:32:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6126164e178e3570337610ef0b171038c4426a730623557513d2ce511166a065`  
		Last Modified: Tue, 09 Jan 2024 02:25:54 GMT  
		Size: 51.3 MB (51303151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ab0b8b073600d46d3039ebad1ab5676fd623885138197d3a6a8fa95c2a99f`  
		Last Modified: Fri, 12 Jan 2024 22:41:34 GMT  
		Size: 75.9 MB (75922888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
