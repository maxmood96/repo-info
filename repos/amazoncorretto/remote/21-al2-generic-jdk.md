## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:a05ae4abdf820458420bd59ab06ca1c8031baf88cddae07718c1227e4cf9a0b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:670e3459f1bb0491c4a594ec23f8383acf426ee2e54419ac34a827cb276aa5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227633409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b44ee2f348c696fdb05b6e21fbb9fa74d75cb309c3125654aa59c6dc0b8f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66682f9e020b8a486a5b8327b9dcd91529551e908725f6943725f848d46cf84`  
		Last Modified: Thu, 08 May 2025 17:05:30 GMT  
		Size: 164.9 MB (164874079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af310bb22ce92dad8cb76b9e98eff923fa495d03bb7e4e97e8f793e43a87cee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5531365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b63f93ec171e850b7411ecaf155a024b55e54dba9238434270ce2dcd644f630`

```dockerfile
```

-	Layers:
	-	`sha256:18f602a1c687e59d5123f7d862cd66820e504c3a70136f34a06938c22f1f0ceb`  
		Last Modified: Fri, 09 May 2025 00:59:21 GMT  
		Size: 5.5 MB (5520117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf50b9269df1b8d923bf0b5ca423e9680c5a3bed4b50fa7409dc7b5bd68953f`  
		Last Modified: Fri, 09 May 2025 00:59:23 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:796643b2d82d02847448a96b6d8d6ac22ecb5457255e230645a4f0441b3ed52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227505207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42476458ec9736c92d0a702d72643e81f93d06b38ffff368b454190b4a80d891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5858ab0a08b327435eea3b3663012a48c60cd126dd5ea6a805063de1d83375`  
		Last Modified: Thu, 08 May 2025 17:07:42 GMT  
		Size: 162.9 MB (162910480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:461e02b75957863deba297e46322776bf2afdeabd91cf3a1b3cbda0e6483d618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438345a0c2060fa65b007c08f51f0484923a71a49598f736b9cc035ad780578d`

```dockerfile
```

-	Layers:
	-	`sha256:4a5575dd65353072911136121e88aaa60f6d5a899f9af8e5df785c1e830a8461`  
		Last Modified: Fri, 09 May 2025 00:59:22 GMT  
		Size: 5.5 MB (5518806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea303323491b6d8e06e08901a3723845748712655bc65a505224e7715890666`  
		Last Modified: Fri, 09 May 2025 00:59:24 GMT  
		Size: 11.4 KB (11399 bytes)  
		MIME: application/vnd.in-toto+json
