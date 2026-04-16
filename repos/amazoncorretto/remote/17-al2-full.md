## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:220d0258ae529dac1e2260c6f61a85172ad0c5a9cb95786d2254037ec585e259
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7acd5b44c0b2e98e57f529d3b9b9d2a8de9146a0a9ccb3f862fe4796deb16a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215410486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e674c28378b0dce8e86b5ae5f2ddfba1ff097b1aa234c300dd4dbab68014a21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:25:53 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:25:53 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:25:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:25:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d44d1181044bb18183f3b8756628e252dfebb612bbd5f528fd1b45de56d3ca2`  
		Last Modified: Wed, 15 Apr 2026 21:26:13 GMT  
		Size: 152.5 MB (152455220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c8f4b17fa22ec438bb5ebd09f443a8529e6bba5d01894297d8d8c270aaa5c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d672c4291cba5f0528168b44b13bb4ae8552edc3b18525ea1ce7c77801acff0`

```dockerfile
```

-	Layers:
	-	`sha256:8cce2baa75bd28584e0bb64c6dd860815728b05aed9af299b5a814473f3ff996`  
		Last Modified: Wed, 15 Apr 2026 21:26:10 GMT  
		Size: 5.5 MB (5535801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c382ee120ca0d37ed4edbc6039a18660a5709c47f22f82deeddb777a03ba94f9`  
		Last Modified: Wed, 15 Apr 2026 21:26:10 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:03ada7fcdff9185e9914dd28f820ad26748fc3278f867b40a7ecfc2c1bdb45f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215774626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a68fee326fa1e2a1c539cb898218bdcf5a4a3f7ac83a880f2383bbcbcdac18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:45 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:38:45 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:38:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60529fabbe409bc96b29d5c1281965124bdc6ce7f59780f6fe0ed404356e0094`  
		Last Modified: Wed, 15 Apr 2026 21:39:08 GMT  
		Size: 151.0 MB (150971651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f41e3f88af11e119080a1362327eb87d1a0420a37d475e6a4cab9a10fe3a1ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a045d8104b1a93a5f30c7de44efe7f20e6d2231b0f22349491a5fb0d15b7752`

```dockerfile
```

-	Layers:
	-	`sha256:ea68ef239ba548008e4c3555f2379402a48fa06742111f7776af7df224be5815`  
		Last Modified: Wed, 15 Apr 2026 21:39:03 GMT  
		Size: 5.5 MB (5534490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:010acc0de614f7c49a234327a91f38e99e7c27f4c544a552cedeff12cdb086e3`  
		Last Modified: Wed, 15 Apr 2026 21:39:02 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
