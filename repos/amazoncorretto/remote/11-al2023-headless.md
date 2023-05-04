## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:bcabb3dc63c8daebf5cef2d4ee8f63e09c2e596969aa862145d703eb5678a3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b698a39bcb3d59ab6b9e2210ec80d4181655ea9c7e5b069dc2ea59a939ffd4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128110103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16df6d99dfde3e7862d1033cba1731a8635552fa1f3ec8e7925401cd80f4e95f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 19:19:50 GMT
COPY dir:54e5777658be1a3cce5e4a60768f16ebadb522eb8101c0ae54ee1f769c3b164e in / 
# Thu, 04 May 2023 19:19:51 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:39:35 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 19:40:12 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 May 2023 19:40:12 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:40:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c863b89e86f3f74e3b816088bacc4f7e984643e02457c9de2f2a80f6f92b9c34`  
		Last Modified: Thu, 04 May 2023 03:04:23 GMT  
		Size: 52.3 MB (52264363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b616195cd0418c45724ba11909bcf03f2b6c4b3c0e1b3df92532b75c3bbc7c9`  
		Last Modified: Thu, 04 May 2023 19:45:48 GMT  
		Size: 75.8 MB (75845740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:79fbc7c6acc121e6f4124c8957813660c3afeec405f0ecf699f45e1ed0c17eda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126305175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a86070532184a9040e8fc67361d67f2f819e80ae4b2122b50254fd3c065411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:39:52 GMT
COPY dir:0b162ee66bcb569c55f662aaca3ee7fff9bf5a498748208a280de7797569e5dc in / 
# Tue, 28 Mar 2023 18:39:53 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:41:13 GMT
ARG version=11.0.19.7-1
# Thu, 20 Apr 2023 17:41:47 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Apr 2023 17:41:48 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:41:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3a410071be52fec7335cb666804896319a1ac81ef15af4c0f1302ffe8834b63f`  
		Last Modified: Fri, 24 Mar 2023 03:10:43 GMT  
		Size: 51.3 MB (51297211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c11aca305e35358449c787e3bb7344730083549cfc6ed2d3eb7962e2502491`  
		Last Modified: Thu, 20 Apr 2023 17:50:54 GMT  
		Size: 75.0 MB (75007964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
