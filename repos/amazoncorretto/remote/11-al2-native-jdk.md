## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:a4deb4c65223e4472f3841c197b4a3efcc8ebe3e094ec32efdd3e8e72258704c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d2d69e9399af7353f0e8c6e8970a97bf41fc8c0e46ec2d2ad54c20f326057cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224599384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9117bcf3ba3830af27d8d6fb96960527649320beac22c2086770ea3efebb3061`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:12 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:13:12 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:13:12 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9fe445fd2895a005a163a44db4b28834e16e44b45186b69609c0d29ce85bcd`  
		Last Modified: Tue, 27 Jan 2026 22:13:34 GMT  
		Size: 161.6 MB (161635675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60d9c124da3d5439290684b98ac6d43a8e1bf29e42696b422f91e0d3d913b9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bf35944938590b188c56b2ce3a0644ef9121f7894de2d7fba953264a1e48f2`

```dockerfile
```

-	Layers:
	-	`sha256:6bfb2607ad6ec00de92af9887654f78aae2a9cb287a16c6b12674da4a011b982`  
		Last Modified: Tue, 27 Jan 2026 22:13:31 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62e020aa55195b80bd31afad84b2af5f8febc6d994a54e236ef3ab26e82913c`  
		Last Modified: Tue, 27 Jan 2026 22:13:30 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d7062f67916a031696a2ae2ad6c8a85ed17bd552f8cb6a52b5a039fa7f24ea17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216528753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244c87f94f8e51ccc90675435fa1c29217636a2b9b03b561ccbccae3de617c39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:36 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:11:36 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:11:36 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc80b1f2a2950eed19c97dbd573684c237650ab38eb03d15428d02b4375c85b5`  
		Last Modified: Tue, 27 Jan 2026 22:11:58 GMT  
		Size: 151.7 MB (151729864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:919e5f36da8b6b0fb8b670055fbc8dc9fa491ef2b4fa496387afd7b3867872eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e544beafa8b67e9ae63c360be0fd2709b2c578eb499a072fdaa97fc31f08f443`

```dockerfile
```

-	Layers:
	-	`sha256:5903f3eabbc6e93262d46ea3c7f919477886bf03643e0b2c6c8280587e1b0ba9`  
		Last Modified: Tue, 27 Jan 2026 22:11:54 GMT  
		Size: 5.8 MB (5787796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695df85a45707082c41375dacf6a0c6e1b908d09b4c8934e1881a7a7948ce9ff`  
		Last Modified: Tue, 27 Jan 2026 22:11:54 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
