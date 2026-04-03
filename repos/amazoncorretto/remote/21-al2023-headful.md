## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:41dbe30d82efcd8d312d356d10702ce034fb134907824e80239408d32bffba04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eae6002b5ed0e48b04c14b74cbd95fa3381e743a693436b28a23f77adb39d4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144003453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd91b392e8f151138cc7825f526076a26113e9fef2d6ea298ae88ba9bd070ae6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:09:53 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:09:53 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:09:53 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:09:53 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:09:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a76659115764226acc84ff2849c15b881b2aea18a8a75e21056e606415574`  
		Last Modified: Fri, 03 Apr 2026 17:10:10 GMT  
		Size: 90.0 MB (89970363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a8e576c9205d8dbb9cdac384cd19338ed878712bc1c7f2c6e8c1618014151d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969c4441747e73819676862e2957c68465dde7a0628072c84f6acc8740f38324`

```dockerfile
```

-	Layers:
	-	`sha256:bec6de9a6fba916737ed5095c4992229601eafba8680dbaf5d8e7b907b622692`  
		Last Modified: Fri, 03 Apr 2026 17:10:08 GMT  
		Size: 5.2 MB (5210021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b327d1529872ac7c7ba2f4abc9ea9283f7810d95289b07e36433907468f32e`  
		Last Modified: Fri, 03 Apr 2026 17:10:08 GMT  
		Size: 9.0 KB (9048 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:16b0f52d1e811cf40ba6c9f6c630656131fdac169ea5a9f750106d97698921a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142054618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193e44524f12cf1b8993f760b7f72abda9cefb6756cde0273431fa96c6812d4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:17:38 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:17:38 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:17:38 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:17:38 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:17:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b9c6bbae087d63b0261fc87480d77d550fe54ab1a9dfa2edcbb5961591ae1`  
		Last Modified: Fri, 03 Apr 2026 17:17:56 GMT  
		Size: 89.1 MB (89113243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13ebae6c540960fcfebc88a47fc65c3fc5475d2509c7fc5c99346475b51ac90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92d40933f4296885f29026699fb3699e6d9f28b762921872a602dc70f704471`

```dockerfile
```

-	Layers:
	-	`sha256:47f9923b495c73f6305658097dfdc62f17519bea677940d83f41f48b7ac059b4`  
		Last Modified: Fri, 03 Apr 2026 17:17:54 GMT  
		Size: 5.2 MB (5208814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6dbf999562bfc97607b5a89f71c55f0a0e4969ec01cfcbf315cbe0bbf332611`  
		Last Modified: Fri, 03 Apr 2026 17:17:54 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.in-toto+json
