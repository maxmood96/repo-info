## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:8f71c4f9569b1e26311d97d92a995e34f7d5f81d2ff5282b74fe0eba617d0cbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4779fac97dd4e790cc0fe9aa52759fec56a5ba5502a299a75d43e9421aba0b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224586913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c69af108298b7a92e30c739eca13fb5af038eeda64cc1ca35720733605ba4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:20 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:33:20 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:33:20 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da347502dc6bc723298945424d0936b5c8cd93b80b958459d4903059cd832f5`  
		Last Modified: Wed, 11 Mar 2026 18:33:48 GMT  
		Size: 161.6 MB (161630403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a3f8c723a91497539e5887e2471b0d8cea557ea17ab91c727de4c7002b2c4e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527e25f783e7aa7783a0b589a7d61b1c0029c36ad2ec7669a6febb83f5f0ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:ec409a7b90cdda1001e3ac6e327e04d89ae2495c51b71f54971753c322cd494e`  
		Last Modified: Wed, 11 Mar 2026 18:33:39 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9be341b68ff4b5312f20cdf2be8ce3569ef7482b8e1aa8a3200a0353a8c2de9`  
		Last Modified: Wed, 11 Mar 2026 18:33:39 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ab97f4a9138de6fbbfd31f73e521ce89f828e76d5b1f1512a92d95bb997b3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216520731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f66b6f1bdd02fe77ded93789a0d1a8f97371e5a2c4c1bc44abfa40f9b09dad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:55 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:55 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:32:55 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212fe24ac7081b1578ec0649e3305a235494b05bbd6ccdc49937c757ec1f38e8`  
		Last Modified: Wed, 11 Mar 2026 18:33:17 GMT  
		Size: 151.7 MB (151717582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd9fd2b122d83c3c41b377be70dfe31d715c5a490815d9a5975c2514e55e98c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff01e6347d40952a8bce3713a5350c1559f8e06379cf478f26cfe8042b6b22a`

```dockerfile
```

-	Layers:
	-	`sha256:c061fef845bbfc65ba72b5afa3cf551245a2f8253057ccefa66a389a61cb9545`  
		Last Modified: Wed, 11 Mar 2026 18:33:14 GMT  
		Size: 5.8 MB (5787796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b01269f710f7bed1268a5cc7de1bf7cb028ee0d1178db05c9278d4e1fcb7f1c`  
		Last Modified: Wed, 11 Mar 2026 18:33:13 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
