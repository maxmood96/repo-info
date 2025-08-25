## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:4f637e315198b6389a0f1865198a41bdc845970e6e3d664ef07400131ae02b75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:631e2f8db16cac55acfecdd76d5fcef29d38844bb23c9c72761431658ff472e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211314837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63dcd00e0aa850e21f2a3c884e44675483dc8612a426ef9a7f715477f49910d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e392f411b02e2eab074a9b83d03cff1a29b558ba7abe1b4b224b81cf9461a623`  
		Last Modified: Mon, 25 Aug 2025 20:55:14 GMT  
		Size: 148.3 MB (148336712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:137e4c6d8947e0d68b315d0468696b99fae7cb671000360da39c1f1136c847d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493cedc30457be28f0f1c6a1fa84d0551e4b8fd38979dc4a5860fcfe23ba623b`

```dockerfile
```

-	Layers:
	-	`sha256:0e1f616c30a4a32902ef8d57e49345624b46f4da9a723181d291eac220b27c66`  
		Last Modified: Mon, 25 Aug 2025 21:47:19 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9612e41b888fb64686d5c83b16d06c95098c5b69406a8f9b2e7cc116706d4aa3`  
		Last Modified: Mon, 25 Aug 2025 21:47:20 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8d8419cae558e7f118ef7253e9d86b9a91136fdbd5adb137fd8a00b0d6fd7376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210167520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f07e7eb11a69bbe1b3bc19d5bbda9d743d00bc19a406df28c6e2a682a4bdca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5551138ad48665f7b96b9a37fbcb5bb022c78cf0912b5dfb2ff11aaea84100cd`  
		Last Modified: Thu, 14 Aug 2025 09:59:23 GMT  
		Size: 145.4 MB (145373156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82553794afd9e8049311c2144d0616d3b2f5854a5ff811c75942509f0db5d12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf85e0cf8d6a428a8b4d7ff6b4ba9900a1507c6090c2e879a54799c10e09020`

```dockerfile
```

-	Layers:
	-	`sha256:b48a06fcacf41701303a4b0c77a22e207914370697d34371c62ef2694654accc`  
		Last Modified: Thu, 14 Aug 2025 09:47:20 GMT  
		Size: 5.5 MB (5539272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb67ef4dd12e2aca8cb598fca596e4d1ee66f8c27a91f679f373155b0316d33b`  
		Last Modified: Thu, 14 Aug 2025 09:47:21 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
