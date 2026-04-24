## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:39879d53aaac847d04136a04c56e463fd7afc0c27c0bf5bf6038111e8155ca20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0c79c511a14818be63f596b29f7f1423e3540a0002bbe7b742563f359d989a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172078467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e28b673bd0b8f7ca54907d00a72b06aa17190c158a63cfd20681e109b220de0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:08:25 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:08:25 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Apr 2026 00:08:25 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:08:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32d5a4a9eb1a70441fca1b00fe5e4ffe098d9f3e016818d3555a882105102b`  
		Last Modified: Fri, 24 Apr 2026 00:08:47 GMT  
		Size: 109.1 MB (109126284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fabcdbd0fa1157b0f20bf120c8f427cd6a0e61fb1abfe151a14ffe7e58de14d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145b6f23cd7739eec0adfbb69bc72c5fec19f6b8e713d8d546ec7f9c6e4f4f6e`

```dockerfile
```

-	Layers:
	-	`sha256:aa03e93a51c0a01d192f73b0a86b9a884a8a7d7629d8f56cea78cb50d00be922`  
		Last Modified: Fri, 24 Apr 2026 00:08:45 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bda7af4c9d5a29be686c6fa9d109871981998d6eb46c4cfa2c46a9d38fd0bf`  
		Last Modified: Fri, 24 Apr 2026 00:08:44 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8fe07cc44bdad1fcb1c4ca205eefcf95f2e6a4c8fa9579289e3f57cb33fd0ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117759062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9e7d9dc698b4063096cb240c584f27b7b76aaddfa835898c0f0e5c1f9ef465`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:07:49 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:07:49 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Apr 2026 00:07:49 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:07:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eac214b8bee9527fabe4072164f7986a47ff33a0a3b0103ea065546b30a4d29`  
		Last Modified: Fri, 24 Apr 2026 00:08:03 GMT  
		Size: 53.0 MB (52960279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b6a599d96a22eb9e95c4732f9ca56980efed166d493d8a49ea10ef9094f0ab2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fde956f4a9b6d1ca520729cb068359513173b5437b8d801187e3d9beb8ea54`

```dockerfile
```

-	Layers:
	-	`sha256:a1a99c543d078c9efe5b5a677dbbc8f155f6c14dc2ab46a38d2eec89f6d69cbc`  
		Last Modified: Fri, 24 Apr 2026 00:08:02 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a0b571040e44bf962f628fcd2bcf0e7bbe5e0c745214e74072a6108a26b800`  
		Last Modified: Fri, 24 Apr 2026 00:08:02 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
