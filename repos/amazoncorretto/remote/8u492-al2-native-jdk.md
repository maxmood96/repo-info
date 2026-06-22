## `amazoncorretto:8u492-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:0cd2aae88756f2f2e2f52f28253577a97edd400763b74cf9c39689b01ad230ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fa9dc9c96f4be0c49746b5db7132031d5afe2d4a72def838ff9b10298b3cb0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188317866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4afca77fe0617721d409c79fcfcb80d5c2342bc0f120312a13c669cd15f6b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:14 GMT
ARG version=1.8.0_492.b09-2
# Mon, 22 Jun 2026 18:14:14 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa0767d1f962f37b4538f145ce5cf6a26bb8e3ccd67a07496f0c8cb8f113e0`  
		Last Modified: Mon, 22 Jun 2026 18:14:36 GMT  
		Size: 125.4 MB (125375847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:865f2860e69c8fc1af2f3f721f46440acd957ac24bff98a2d18c342959bfd70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adc78f14739e90be64609e879557d5f4f61b2c3e62dca670927c0120db65c8c`

```dockerfile
```

-	Layers:
	-	`sha256:25af48f05a4f67b3dffda047e09d33e5b683162349abc2361d631bdda29e9bfc`  
		Last Modified: Mon, 22 Jun 2026 18:14:33 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb840a1f7728b04ae74d349e8ba2ea736e73db4cc7738bbfbe4d56db0429bc18`  
		Last Modified: Mon, 22 Jun 2026 18:14:33 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c7e6d655240b0fa0ee004322087c2c4e4b8e67652abaede187d0f260f8f257fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132452055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cf078e0344c5b7950002e01e63df8a954150ce555057a57a7dccdb3fc23ef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:13:52 GMT
ARG version=1.8.0_492.b09-2
# Mon, 22 Jun 2026 18:13:52 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:13:52 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:13:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ffef9b1585a02076365e1ffdf40b5ed1ca16a0e3d8abeee0cfdfa9a3ac9fc`  
		Last Modified: Mon, 22 Jun 2026 18:14:09 GMT  
		Size: 67.7 MB (67657319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dcac25f7f1f7e9f680fbdaa275d22221d0e70f795da91e9887aefb54862008ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a1b51fea5a5a652ceea12bf59c6a9095be4e2c4878000bf193b22022ce78be`

```dockerfile
```

-	Layers:
	-	`sha256:c4053760ab9bab775a9c8379b77a2fd0cc7c56a6877b3664c0a658fe9a4523a7`  
		Last Modified: Mon, 22 Jun 2026 18:14:06 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:763c96a880e279ba07a8e776d40d86d54418266abd417ae8456ee1108b2e5259`  
		Last Modified: Mon, 22 Jun 2026 18:14:06 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
