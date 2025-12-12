## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:75af347f1303880e22057f16a840fe23c2786ef3621c2f9a5daaf8eb4eceaafc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b636468668e64df456e0bb11e76caf0a9e68ed047e65e121a82119d7410abd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157576829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae78cc8b14de967f27e9de855fa537aa61b7c7cb956c8a7742853b8104cb8b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:23 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:23 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:23 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:23 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d053a798c7967db61d7d3337855c33d6e5640d058cf616fe97d680c7da33c15`  
		Last Modified: Thu, 11 Dec 2025 22:13:56 GMT  
		Size: 103.6 MB (103588369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2d227743c3331c0c2deba020f47b734b133823db43ceb5ff821f070787107780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421c41986c0824857f9969cb0bee4c27715feed7837937a3ed914650a9b99e0`

```dockerfile
```

-	Layers:
	-	`sha256:dbab9e72c3c7bcd678c928d3f03c4a458bbd041320aedf8a3887672ab09e9c3b`  
		Last Modified: Thu, 11 Dec 2025 22:50:55 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c08445d2ca4e492e07f21ac0ed0dcdf0f0b6931ef2cdde05317e5fa522a35a0`  
		Last Modified: Thu, 11 Dec 2025 22:50:58 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a1e4d74f67d455e48615c5af1ccf137f92f07bd74db3c3a88ba553de1ce62ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155402214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c491b18bf440ba1867a4726a363a812337ab97ba0ce06f0d6b6ec2f2dcfbed88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:01 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:01 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:01 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:01 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e11c8941afc2dd565b4de3804e91f76b43252d61f9799c5123e98fdf52b4e27`  
		Last Modified: Thu, 11 Dec 2025 22:13:38 GMT  
		Size: 102.5 MB (102528764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c84fba4ef3758e6adbd7a51c13402af80ccd32aa8852003d8e980792af03d8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfeff9c4873ca165b15d5a79a579f9b050b633dd1cfd2646e928338b0fc947c`

```dockerfile
```

-	Layers:
	-	`sha256:8c04c404ba0d2988e9aecefa087cea94537bd75dff598f1c1a7d94276575084e`  
		Last Modified: Thu, 11 Dec 2025 22:51:08 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4563d08db50aea2a2b589442094048cdb587b3273926ad0451167e2ab29ea458`  
		Last Modified: Thu, 11 Dec 2025 22:51:08 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.in-toto+json
