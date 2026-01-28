## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:769d1a970b7bef44739be68c68adda5183c2ae9ccdf45547f8c60592483665b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:02135f24ffb381c6f12ce194feea84e4f9e69fbfbeecb86b8dd99f5fe1ec0766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224599238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b28c6cafa041eb01259b5d9b277ef871fa0da4716faffc03f6a78a80d01935b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:10 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:07:10 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:07:10 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cde105b37deec9e22ce4ecc6770bbf00b59c46c877974379ade89f82b5ce782`  
		Last Modified: Wed, 28 Jan 2026 04:07:32 GMT  
		Size: 161.6 MB (161635529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8b16746550530ec45a807b56da9c4c54c623b4d4dade8b2f5a427cd96e12ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab5f6f3d6663057586f8a18a7c5744d06d0a84dbc28fda6f48cfaec57aa4ac3`

```dockerfile
```

-	Layers:
	-	`sha256:b634fcd3deac1c0a3a49e316df91f9dd43a9c70c644882db6fca22194557e75f`  
		Last Modified: Wed, 28 Jan 2026 04:07:28 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c0145091befbade5e854daa59a5aaa8646503de9ce30e3950d23bf38994684`  
		Last Modified: Wed, 28 Jan 2026 04:07:28 GMT  
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
