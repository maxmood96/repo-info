## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b9617b5077de3ba8f06cc07bf6322c68d78402172acdac3b38d80a25e2e9c413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6f8dec43dfd07002bf08cab9d5f82c329e0b06b8f70fd0136b7cb6d05edb80fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228695860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a3c5f8f22b43093904b1e22143888ed2c3e42666cc7bd2fe68ce31913b2cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2225fcf77fe3b44fe009ef0c7b7c2f5dab46a445fc4edb11ace04b1473b0c`  
		Last Modified: Tue, 08 Oct 2024 00:00:17 GMT  
		Size: 166.0 MB (166017704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bcf93b99cf82bb285d35b413c430be4e486faafab7536489b550a334d32a809a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7229d253d3fdbfbfcd661d1bf10bbe584680cd0658ac125d146b8801cca2dee`

```dockerfile
```

-	Layers:
	-	`sha256:57a2882b42a5c7977c39a1793a6c81b52bda28c17cae7cb17668d547e8ce6449`  
		Last Modified: Tue, 08 Oct 2024 00:00:15 GMT  
		Size: 6.0 MB (5966117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b52c768c90e2a53616a8cdc65edef1f3a0f07fe32187643e045e28bca58914`  
		Last Modified: Tue, 08 Oct 2024 00:00:14 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ce80d8d68f43eb8cfc3e4b0f9cd30aa9a368899d9e433631ff65504065222173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221199408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89516482a0a3add0483d5f44f5d9a16d87b9f92ff05357cc3868d164481bd0f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4590bd7137399f10cfbe4f4882d11c9c6b16c4c5ce1b81a7c1ab9ac164e31a97`  
		Last Modified: Tue, 24 Sep 2024 02:41:46 GMT  
		Size: 156.6 MB (156612861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7819fcf9e6f6299407a9bec631931189932f3957d64e42d844cefa725391b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5767917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5064c767dbbe41e378db79b237044ad690920e4707c2e0aa0951d1c872e6ca5`

```dockerfile
```

-	Layers:
	-	`sha256:44ab2f1ff64f5d4a8ecc6c80cf2b4bab20701c9ffd4db15549d95235f0549adc`  
		Last Modified: Tue, 24 Sep 2024 02:41:43 GMT  
		Size: 5.8 MB (5757633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb30253416044591e0c1bb1e18a219e8463156b43da5d80b6f781a4a5cb2b8f4`  
		Last Modified: Tue, 24 Sep 2024 02:41:43 GMT  
		Size: 10.3 KB (10284 bytes)  
		MIME: application/vnd.in-toto+json
