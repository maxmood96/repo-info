## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:d0275f3d4e77af40a891a1dcb8624f2b81030ae492dae048b29dd2257af4e425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d89d3f6ab758f72940fdb3c6baf69f5f3e8aab485f508738b9dd34e3808dd723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210808805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c39f206517537667adc1476c9e0a91d7527b1e02b628d7dd5fd777615cf639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:22:03 GMT
COPY dir:9acefc3d435d9504bd7fba575b2c4ee96a407449bf3ba0c2338d49d9a97b2a5a in / 
# Fri, 05 Apr 2024 18:22:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 23:55:50 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 23:56:13 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 16 Apr 2024 23:56:14 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 23:56:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b48a4417297666404bb1459ef5f08938bfff21f2d5adb051db9f61fc54934d30`  
		Last Modified: Wed, 03 Apr 2024 01:52:33 GMT  
		Size: 62.7 MB (62667250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f97f961fb89e85592de7b81c07728cdabb47eb1430fe655eaea55e0f738be6`  
		Last Modified: Wed, 17 Apr 2024 00:15:28 GMT  
		Size: 148.1 MB (148141555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36835e227a0fa470ee0169121700fae4c4b65c2fb860dd6e470b083663e1b156
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209787208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36e226ad9d12e6d2918ddf554d0173d7324507009e8c7b2c4df0ff698757afe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:06:35 GMT
ARG version=11.0.23.9-1
# Wed, 17 Apr 2024 00:06:54 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 17 Apr 2024 00:06:55 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:06:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0fbae38e2e41bf3ab58de943131a76ff0e6dee3eb1cdef03870530d54a461f`  
		Last Modified: Wed, 17 Apr 2024 00:23:26 GMT  
		Size: 145.2 MB (145226599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
