## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:137f0933f62a0367b35cdf1bc505620333d6c6b6e701903acb58aad4d3ef9c6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1101068a280843244130065d2d7a81a58866bd190ac28876961815013d87cade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215411249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c7e5967388514e92d8a97e9db994edfbf1a5d85a409f4fc7b430a5e2d61a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:09 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:09 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:14:09 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629127badbb34f2290251a80df183d34aa4ca03ca8cf38411493f3aeaca26cce`  
		Last Modified: Fri, 03 Apr 2026 22:14:28 GMT  
		Size: 152.5 MB (152455948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cee70f2c3943aba4b8901175da96bebe66bc5bf4779ce276105f4c566d88788d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648afa244cd7ba8359408fe3a873336e52438f4735e1e96e25752797bd90ee9c`

```dockerfile
```

-	Layers:
	-	`sha256:960cf5643bedce4ce236763c4775fdb0886c1381396e56af2b0697581c2b4937`  
		Last Modified: Fri, 03 Apr 2026 22:14:24 GMT  
		Size: 5.5 MB (5535801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05116acc05f6f24258cb0b6f846ac3441a6664d2309eca3fd47b060d2558843`  
		Last Modified: Fri, 03 Apr 2026 22:14:24 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cb00d2ee803f78276fa52016bc872679a9723032f2bf3df70fdbc9c150968293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215773734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df626397d40db0cd8c53b06a88dc4d7ebc6e3858b31ff0e2f1e386b8f66aa21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:41 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:13:41 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:13:41 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1200879671d0b9b8f7eb006d486fe28538ebbeef1137aaadb6db419ae8d50b`  
		Last Modified: Fri, 03 Apr 2026 22:14:04 GMT  
		Size: 151.0 MB (150970895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0d341f5862220402197c82a81d2984507366891f46a74870c9006e61d31389e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf8da006d81fe745985522bf734c3e88d9b2a48a040ace8f5fcec39417be15`

```dockerfile
```

-	Layers:
	-	`sha256:c03cfbd6bc8d53ce13511223ccbe00255a9273415335ef8a16d7a23b26afd46d`  
		Last Modified: Fri, 03 Apr 2026 22:14:00 GMT  
		Size: 5.5 MB (5534490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9faaa6501ca1d7e48fc339178a2befce6017e79db5fbb9a2b1eae71f2eec9cf`  
		Last Modified: Fri, 03 Apr 2026 22:13:59 GMT  
		Size: 11.4 KB (11363 bytes)  
		MIME: application/vnd.in-toto+json
