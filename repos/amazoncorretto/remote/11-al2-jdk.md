## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:29cfe63f2edb1b2dc6d4cd69c43bd1d12f89fa6fbb07615a43b0789955be0e57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce4c1103dbab7956435938a1c1618d28282daeb1f1ddd8e35f5af949ab4f00f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210991376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d36ee428f8b26ac6c614270885ab0f9f8417648abcc7fc3ebbe2d8ed206a5a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:35 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:35 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:35 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c255fa6d8e6e339f5a6ce3b0f612686a656a0104727502b239564d9b10ca9e`  
		Last Modified: Mon, 04 May 2026 20:11:53 GMT  
		Size: 148.1 MB (148131367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73d4a5ef7586a102b9e51c4e4268e9c0ddfed724c525e3aa68b45a0039755365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee37888b53c363f918605f4fdb7391e7812477508d9f4ead8589b44ca8ca0abd`

```dockerfile
```

-	Layers:
	-	`sha256:447256a45a15b42f8709b24b081b1c33eb8334f0e0cfac0d85aef5ae35c39912`  
		Last Modified: Mon, 04 May 2026 20:11:51 GMT  
		Size: 5.5 MB (5543110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5620fb93107af1fc592b786ae9f14b95b3e1ac3f93b6bf6140bf66d6d660c2`  
		Last Modified: Mon, 04 May 2026 20:11:50 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a4f397e2ff8d42b9831cc64f098d59f26277a7f41f2de5eca09cf11570940747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210159228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c1c5d4df074ff96ba0ee7fb2d7d92bf043f792c7bfc99738b68ccd24fef04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:06 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:06 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:06 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdedb09c7b30ad59316625c4e6199c7aa3f67dbbe393920650abfb9e6b29409c`  
		Last Modified: Mon, 04 May 2026 20:11:27 GMT  
		Size: 145.4 MB (145363697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:50b30cc56e6eefa634dd23eceb006c33545a9e6fa1baac2863da82ddcd15b968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dac0bec4da8d42ee54517ff9d44e8e60a30af896c5faa841750d36b9a136cd`

```dockerfile
```

-	Layers:
	-	`sha256:6555686ac65f816e5ed72ae4808ca285f614fb3c81ffb5eb575f5c73d0e1a798`  
		Last Modified: Mon, 04 May 2026 20:11:23 GMT  
		Size: 5.5 MB (5542604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142a35ddc7109316d48da93d1b7d960fabcbd43bfe44e482d3aded869c02c322`  
		Last Modified: Mon, 04 May 2026 20:11:23 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
