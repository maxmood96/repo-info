## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:30cb43d953f33c9e40caaf5f0b9e2b83153aaa55849c920f9da9bada49e839b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bde709d9dda2064e72e482d4f79150f69c4b2d00e74795f278ec0faa6b23195e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158323740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fd4c23af26afa1e463e3083faed5b7a11a3d327ea11f78bef7a15494b2e7d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:42 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:42 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:42 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ebb308bc7711d9f9488f6ed97383fdb2a932c78dee9a9aa7ea55715d2b037c`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 104.3 MB (104302536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b8a1503f6853107a46477dc86e460aeff1b6d020a4d7cbd8c802e5b87312c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a8e1e422df90a0434906ae08a2627b766fa6d65c18fe49ccf4a2ee48f6e38`

```dockerfile
```

-	Layers:
	-	`sha256:92b6018a75649acb75f19eb103e7cb39336a86113f4a2e0a381fff1054d06688`  
		Last Modified: Thu, 15 Jan 2026 22:51:40 GMT  
		Size: 5.2 MB (5220212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a29f94ef272f56407eef44ddabfd5c1904a030a98e982338079fc2efb30ac`  
		Last Modified: Thu, 15 Jan 2026 22:51:41 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8c742367a4c5e1bd982326b492202f16e670df26e2346dbb48cfffaa7ff1312d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156157737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b795ef5048d3acfd358149c715be93e943ea367be015bf5e207dd3627a2993`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:15 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:15 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:15 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:15 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa64361678a9467c268f470a5a1b017dd3aef73910ba98215b59b21a058f2ed7`  
		Last Modified: Thu, 15 Jan 2026 22:10:55 GMT  
		Size: 103.2 MB (103243380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ead248ff476f6e52d49a74c46f5c0c4ad5d76c5337818509fe12ce6da18733f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef0b91a570b3edbfa01422309766d1dcb481caf55ca30f4797ec3f6e2cd19b`

```dockerfile
```

-	Layers:
	-	`sha256:05c5723a06c91ff32135f46ea74b13f2c748bbed6af1e0030a0313b3787790fc`  
		Last Modified: Thu, 15 Jan 2026 22:10:34 GMT  
		Size: 5.2 MB (5219026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b427e8b09d2032068cfd57d1e7ec900361f6555ec65eb9efd4ed46f95b9275cf`  
		Last Modified: Thu, 15 Jan 2026 22:51:50 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json
