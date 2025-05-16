## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:cd17b541a8eeaa8090978ea8189f985947689e2b946b200202e822047dc0632a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f134457ede8ce75dbd3c67d4690f75a5a63e29c4a58806b93b8e12fde87739f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153935459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cd33f6a363dd30f66eef67755a85f2c93d33e4ffac1694ede22eb6aced25c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79446580f9be9e70a57476ff6dfc6df2fb6b368590bb5c2271717d166efa9dcd`  
		Last Modified: Thu, 01 May 2025 21:08:20 GMT  
		Size: 91.2 MB (91176129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c84d162131155709ad35ec949b1fe8b9438268023a7d9034fcf372f6f710eccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037b64c209f412380a688daa105739ce92106cec5bbabfc92208d34e26c901d7`

```dockerfile
```

-	Layers:
	-	`sha256:277a063aa74a0370f6b4700fb72befbf2c551549877e69b35b164f898211bef4`  
		Last Modified: Thu, 01 May 2025 21:08:19 GMT  
		Size: 5.9 MB (5852682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2263c76b31a7c68d096595d1178fb191c05930bfff75ed06c6b09f54b6dea980`  
		Last Modified: Thu, 01 May 2025 21:08:18 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b386625cf585bd2930fc88f47596923bdf88eb1b66608db6948cbc7a322aa4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146508100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cadb3ce52a4fbae1f303e9b9381af96eb44cea55f1dc3b31e9a275ba29af39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd705ce507496bcfabc2466c5589e131bd28ab602f0a6d3c707f98c2fb2439a3`  
		Last Modified: Thu, 01 May 2025 21:20:04 GMT  
		Size: 81.9 MB (81913373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:baba21cb5c2011913468e90dce9df55bf01277df48f734210d1ed0c323fda364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5653976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5ea9b134f72990127caadfc7ac38ac495c2b8eee4028cacc5fb2059c4583e2`

```dockerfile
```

-	Layers:
	-	`sha256:4cff13beb1e80346621f220b14a43fd8e13e791348dde0382fdb4a5039c1bd08`  
		Last Modified: Thu, 01 May 2025 21:20:01 GMT  
		Size: 5.6 MB (5644425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d016a8ff10387adbf2f7d733ee4a8aa1d0157aaa03c9995fe5aaa11e3407dc7`  
		Last Modified: Thu, 01 May 2025 21:20:01 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
