## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b7fb83f57bf56ff5bca52e2e5101ac19059410ffb2f66da2a147a9640aa2a82e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:72e97725ec1515a026871ef0a9c7afb04d497ddde7e5380dc66f1a55beabe7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187907857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1108db43bedb066e962b9dfb95c0a9a331519cfbb8512050af90cb13b8aa6ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6252bf1f0f9b41e2a8f6374a8a252f1ae25a67239bcc02d43af3b859d1b4c3d`  
		Last Modified: Sat, 25 Jan 2025 04:14:29 GMT  
		Size: 62.7 MB (62669455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3ae8bd7568aebeb6d90a0abd64c341c2baea20ac13378dc8b48e5d2b4edeb`  
		Last Modified: Sat, 01 Feb 2025 01:09:09 GMT  
		Size: 125.2 MB (125238402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13bdf5f442d9d76a18f7d27068fdfd17d7666d9ac6805da16f5a32fc58e68415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869937bdd2299543068b302966cb7eca3e5e4a02d58a6daee8414870968d173f`

```dockerfile
```

-	Layers:
	-	`sha256:0f647e7e8a701477f3b1c7040f3ae3a03cc11d96f03def16c67cad22cd5f85d8`  
		Last Modified: Sat, 01 Feb 2025 01:09:07 GMT  
		Size: 8.0 MB (7956590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79a10160f097d189756ff914367f6645b1e09116b9f284c457bb0b9223157ff`  
		Last Modified: Sat, 01 Feb 2025 01:09:07 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b84de1df4cc2373e6dd690aad0bfab37c5952812690d61a9516ff3e21655a170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132138391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70760ab771e7e350a4daf421249a92ec06175d4054edce8be56f866577b2180`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e694aca9e8d5c223f3e2469e032276879ab4b403abc21549d4277f4463b2974b`  
		Last Modified: Mon, 27 Jan 2025 15:17:25 GMT  
		Size: 64.6 MB (64578423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c5883681006134485d1a560a574f6afa5dab5e42302970a4c428a91c095608`  
		Last Modified: Sat, 01 Feb 2025 02:10:16 GMT  
		Size: 67.6 MB (67559968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:38c919636fad1a6c8f255ca59b986a389f5946a15eb6fe8808a89bc3cf277aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6bd44da75b3a1068d108180d4b1e88f0ffc6a7ce80a42464498af142a628e7`

```dockerfile
```

-	Layers:
	-	`sha256:992b789d847a50ef7a44ad9fc9abff500b7e4424eb6c3c6a5dbbf78cf0d68038`  
		Last Modified: Sat, 01 Feb 2025 02:10:15 GMT  
		Size: 6.1 MB (6066675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b294745779bbf615bde3a55f8446a957a4cb65317e369a0dfb4d3afd042a4f`  
		Last Modified: Sat, 01 Feb 2025 02:10:13 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
