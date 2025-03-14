## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:33125c389b8242e8539cd6e30ef8514036ba6cf00638a5eeab975e087d06bbdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ee1de0aa6fcbf3a5ef2a238dc168de1884fda164a6e4f8bd8fb19d58c3616436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138418247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be6c27ae825fb7a327ac094946ef98e203dc2d9f61fab12cccd04c32e7610eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e70b802ef91fb15807618fc5b70fda13e347c7002e575a087d2eb45acf6ad`  
		Last Modified: Thu, 13 Mar 2025 22:52:51 GMT  
		Size: 75.6 MB (75645409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9bc0ef5b9c83c68008af67a1bce7960df6896637019cf158f9ad2a5c8434e1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dced7afb1652f44eb542091e9856a84dab35fe97b4a956fa8dd8375ecbb181`

```dockerfile
```

-	Layers:
	-	`sha256:f64614622216e8dd88070c40d92ac923decc71ac9e5fc496d314131fd53eae7b`  
		Last Modified: Thu, 13 Mar 2025 22:52:50 GMT  
		Size: 5.4 MB (5359568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a0a6f148bd04956a9631f62768add635d7020e4de3554e696dc5f618dbfcfe`  
		Last Modified: Thu, 13 Mar 2025 22:52:50 GMT  
		Size: 11.6 KB (11569 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3b180573830fdfa3180b4c4460aed169f61124c2099bd4e959ec326c05e1bfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124266748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a758d19058423f5ba0e23c74b13d7bbdc91f42c26ed6b4e7525b03540e3b1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b353ef92e4c2e18f758c76cd0dc6c24db417361a6a94832d8c141791d999962`  
		Last Modified: Fri, 14 Mar 2025 02:46:43 GMT  
		Size: 59.7 MB (59689894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13e7e39c5fcecb3ed8a44e2d47364f1c8ff8d8193e1d5d0ce230f1a59d5bacc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733e59b0c3c8fb4aca9f7c2feffd579a20d6f734e5c3153170aefe1bc41cac8c`

```dockerfile
```

-	Layers:
	-	`sha256:c0302ca0155d2e0edf7fdbf18ce0d7c212a60a6a830b3c3fea6aba7c43ec635a`  
		Last Modified: Fri, 14 Mar 2025 02:46:42 GMT  
		Size: 5.3 MB (5338067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069ef597788af762d6841a363e282780655b1a732f0418ee6e78268314553e68`  
		Last Modified: Fri, 14 Mar 2025 02:46:41 GMT  
		Size: 11.7 KB (11733 bytes)  
		MIME: application/vnd.in-toto+json
