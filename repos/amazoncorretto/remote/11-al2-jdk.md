## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:8219f64928b8bd9d998373fffb72490f862fa129e7c9fedf64c9c51a2206628e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:072dcff9fb1692a95ffba7df149243e3bad5304acacc412e86173c921ee4ff94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210991360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76fe5946c847407038b018869d1d3a6d1a07188cc9e2ab164b53c935da45cc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85e2aeb790b7bf7dc9962ecd9501c463a3969427012e6ac0a0fa0e8c9cbe5a0`  
		Last Modified: Wed, 22 Oct 2025 00:47:52 GMT  
		Size: 148.1 MB (148050740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9eba476804ddc7361dba0da314e779332f36ed3ed09102f418411191a08a67a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699bdb9818ca25ad040b7787c9d7f47d40de7337c4b3410ea60581535e946400`

```dockerfile
```

-	Layers:
	-	`sha256:34f2a786a575b3fff720fd3eabe24d8c3fb3c60f58714f5e52bf0e71e9767eca`  
		Last Modified: Wed, 22 Oct 2025 00:47:19 GMT  
		Size: 5.5 MB (5543005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d20f8b4229e1c2283b094b03bfaf438b325240a536f32417b5ce4ff205c838`  
		Last Modified: Wed, 22 Oct 2025 00:47:20 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:59b03de4f0981d918392489076998722f979cc8951237390d390df74d55ebee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209937846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b1c243add1d7f4d5bc160983767d1ed8013bbfcae165ff5ec5b9ff73b4b0b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b8b12b7c5856e259b06bb3d673e93d1bea0809ad17d2d440d5f224e3e20fb7`  
		Last Modified: Tue, 21 Oct 2025 22:13:35 GMT  
		Size: 145.1 MB (145144638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7285cd9a5202d68a09cbcfac72962e7e507f6826eeed3ae4961f62e6bf5259f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6708478a00e31c1403bdc47be7d47488f2a77e2d0265b99bc5f16f1eae64d05`

```dockerfile
```

-	Layers:
	-	`sha256:3ea83987f591b07ef14d31507d3456955f238559429d08f11a3bcb1f2127556a`  
		Last Modified: Tue, 21 Oct 2025 23:16:23 GMT  
		Size: 5.5 MB (5542499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da6ad4d743e4e9908bfff58cfe5d1cc3844c51d846e96effdfb55427857d2c`  
		Last Modified: Tue, 21 Oct 2025 23:16:23 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
