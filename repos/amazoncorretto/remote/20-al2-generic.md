## `amazoncorretto:20-al2-generic`

```console
$ docker pull amazoncorretto@sha256:38189d6c4d4a7d1bc0eb6fb16b8a010d55aa7fb06c4e00ce7235a9d4bb3daec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:14e4ccd97d754076610da39cbff7471acca1c553e1d756405d8fa4f7d6113efb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223362421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560f1ec0fb999f94fcedcde8dee29579e616d74094343ddb2af8bbff58225765`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:22:38 GMT
ARG version=20.0.2.9-1
# Wed, 26 Jul 2023 20:23:02 GMT
# ARGS: version=20.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:23:03 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:23:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5d88c566438c06eda6c652c8b77b80eb697ede34d91cddca7f1f3b6190b0a8`  
		Last Modified: Wed, 26 Jul 2023 20:32:14 GMT  
		Size: 160.9 MB (160910501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:81839b554e4b79e15fd9f14a42519c371565c2c5290490a509520a9719b04061
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223097466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57446731ffcd545417e8d4293e294ebe3aa1c55ed604d26c5412f29e0bcce5f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:59 GMT
COPY dir:680654fa7b59b44a83c6e6e3392ca226b5dd93f22761e5f1147351db4c3466cc in / 
# Wed, 26 Jul 2023 19:40:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:24:26 GMT
ARG version=20.0.2.9-1
# Wed, 26 Jul 2023 20:24:46 GMT
# ARGS: version=20.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:24:47 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:24:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:51a637e5b43ccbed5bec2958dc012693f30cc3c6b3a2760e6d675bedbae44e84`  
		Last Modified: Wed, 26 Jul 2023 19:40:35 GMT  
		Size: 64.1 MB (64129279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cf372fd2879518e92b0fd0724fcb73d6e185b25ac031f7a1155d6ef09de129`  
		Last Modified: Wed, 26 Jul 2023 20:32:23 GMT  
		Size: 159.0 MB (158968187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
