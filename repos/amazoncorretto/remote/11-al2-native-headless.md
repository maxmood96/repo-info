## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:6d5582b0ac1d23665bfcf6477c810f2b06548601c6b28fa180ef93fbd1aa6305
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efa0042ac56337d251cbe73036bad8b6012b33d54b1d4b7221e445bb1df56526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217299533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95974ec2904f5354590526b4bf24a435c9d5d9dcf916e5c585025e59e2c6b92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:06 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:13:06 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:13:06 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef27162cbe064e946a95ceb63a84b9e2f22098e69383531d5cf6a473cff40dfe`  
		Last Modified: Tue, 27 Jan 2026 22:13:25 GMT  
		Size: 154.3 MB (154335824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d08083d7fc7194b2dea880e3db3fe5ce20cfa33b7d905ed3f46f1a34e34fd2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6169dd730ca620ade16831a4a7eb6c8eb760c2a608655069f78757ad6df1385b`

```dockerfile
```

-	Layers:
	-	`sha256:9f5e19084818022be771f1b19b0a0fddb0c1490907ea77c026597dc6844082ba`  
		Last Modified: Tue, 27 Jan 2026 22:13:22 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d94d85cd07eb04fa6ce690040aa717db7a745a052237273566c3edbcddc3c1f9`  
		Last Modified: Tue, 27 Jan 2026 22:13:22 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cc7acdb679410206042558d7d97c519ec7b35dbcfa4631d9efa316c08b01004c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211421493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7782412516c603ad18d113da1687f294c25edb56bf4cdb7fafee04069fd58f58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:10 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:11:10 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:11:10 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfd30d4cbac9f7e3d55339bb9f61d2162508d8489ff04f6b23b0d71c179f207`  
		Last Modified: Tue, 27 Jan 2026 22:11:32 GMT  
		Size: 146.6 MB (146622604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8efe7c3e820e15f457734cd7b21f2d0942015500d0fa913e38db2126838849b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e028d8f8fa1777b8f4ebcad88a83c3a9248b35da964acacd839677954f055d`

```dockerfile
```

-	Layers:
	-	`sha256:61e87f5c524c6223ab15f96ca6baabda2870a634b563cecbee1fe6414cf5ac77`  
		Last Modified: Tue, 27 Jan 2026 22:11:28 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05af84bd2f378a9e3c7aca394a112e0ccc8a9338be990abcac8161a657a255ac`  
		Last Modified: Tue, 27 Jan 2026 22:11:28 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json
