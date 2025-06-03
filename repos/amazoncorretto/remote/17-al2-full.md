## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:421e9c0d57eb6892c33a24f01c499854d139d1e7f46bb23436b142197c89179f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:995c4ff3e1c0485fb68f0d84d5ae3546a6a90b4889d3c55fd36f95ae0b36ce9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214494238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c93aed26a21c0448f47d3a09d89a94ecb72cd5f1ea39f093489fffefa352667`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5e8e7a00da5e54199b818ce7941f270d97472be3e2f3676fb333e1a3869ddf`  
		Last Modified: Mon, 19 May 2025 23:46:10 GMT  
		Size: 151.7 MB (151734253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:877a7429af854795458adac6fc40e7dd3b5a686f14937afc66b1d5d62381c1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5539294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b27e3738d097d06d180f138d188620492f9985773091fb3205241cfe01ab78`

```dockerfile
```

-	Layers:
	-	`sha256:b295236080f5d0cef1b3ad6b713e1c527e9cf2df977241833d52c4fa3591a5a3`  
		Last Modified: Tue, 20 May 2025 00:48:16 GMT  
		Size: 5.5 MB (5528039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abd8250ff29aaff24ea835d8673627ab722e8130b7e7cbe11a1837b0954732a`  
		Last Modified: Tue, 20 May 2025 00:48:16 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b675eb632bdd57876014e92d6cb700054337b84feb7875d1855c05ca2ece4c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215006713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0616d1834b6d6fb8f43a086e2fa8cb8cff81f903f39962a1c7ca8e8e208ea0b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee6e95ea36d89af4f4cd7e8f243672db44afdd48ed329c3637ac24e8cf28ee`  
		Last Modified: Tue, 20 May 2025 00:16:49 GMT  
		Size: 150.4 MB (150399232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ce18afb7e294cc706371412548d0d964ed677cfa2e302e9ed28f84f5501a3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c1bcbe4b689e6604b5a4ed380a8d70e43a070f7340aa37cae15af2fcc60e87`

```dockerfile
```

-	Layers:
	-	`sha256:9d970c0e45c3aca1ecd215473acbbe761fecb9d5d8ef38a518d2299519522f67`  
		Last Modified: Tue, 20 May 2025 00:48:20 GMT  
		Size: 5.5 MB (5526728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2081f9a47b3f6d49e25326fa250607233836ac7c998a1457796e81779f768cb`  
		Last Modified: Tue, 20 May 2025 00:48:20 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
