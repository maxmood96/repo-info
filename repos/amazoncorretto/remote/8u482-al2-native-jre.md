## `amazoncorretto:8u482-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:bed73fd6eb17931bdbced383e9441dac32c4cfc16e4930c71b23bc6a7c91658a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d33ab3203d5affd2814e0f68577299a06c8525a9a9bf52df3d6a3e015e22b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172097726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18d5fccede645da4acd0015fd8044fcd4d9881655eec72eecabef187b961c4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:50 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:06:50 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 28 Jan 2026 04:06:50 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b3f213cbb9a113358a6d960feb7f5e95977aefa65cba434768775d0ee0ed1`  
		Last Modified: Wed, 28 Jan 2026 04:07:12 GMT  
		Size: 109.1 MB (109134017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17b65e09c768304e324668665cfd2d33033a3b865590acb28964c9c10f85c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007e9c900b0d1171cccaabdfa034c87a60ca3a33b6b39a7047292999c2906332`

```dockerfile
```

-	Layers:
	-	`sha256:b38e62c1f19543d0b906ea951c83205bf03c5a3b3c19e503f3d9d05cf95df24b`  
		Last Modified: Wed, 28 Jan 2026 04:07:10 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eab617da81d32810dc835f4578dbad2ab650f1c76a02a01415264851625c9b6`  
		Last Modified: Wed, 28 Jan 2026 04:07:10 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9be3b1892ea28760bf7338cd01fb4503aff2f9d69a7cc3cbe1a27957b896110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117774120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb6e5cf9fe94fff4bb39deb62caa7e76d6585831fabe6169f50d52f326f1174`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:33 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:11:33 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:11:33 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d9f4a84b91e52d8593d1fb244605fbd152414262d12f173ae07cb6c54f5c79`  
		Last Modified: Tue, 27 Jan 2026 22:11:47 GMT  
		Size: 53.0 MB (52975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dfd22b8ad17ec8565f9517b7f2655914720a5076233032a0328c53e0216e5cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa3ee17afe717190ce00f7d5001e985a1cc2d1a78237c0799134441584f70f`

```dockerfile
```

-	Layers:
	-	`sha256:65ea2b171785f7665d5e8d12ae03f09e9a391dfd751315aa99785cb9112fbfb6`  
		Last Modified: Tue, 27 Jan 2026 22:11:45 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e65d7a604e65985de8e4c94cf1585c2ac4ecdc5864e1a3d8cfe696ab5b1e30e`  
		Last Modified: Tue, 27 Jan 2026 22:11:45 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
