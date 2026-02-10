## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:bd1915d69cdc5612307ac96524690342c988db1b02bcbaef95a907b8717c786f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:892d69d4b07fcb69fac698df7f3b584e562b3f8e88bc910e508c6b8ba27bd201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139097859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6ec80be09c3c6d5e57151327f9c98eed97967be95f8348441b4b558e310f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:34 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:34 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:30:34 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7faf293aa85d1b8fb9da66170ba497f59fe1f7baa68fa40f05f4030be8e3c1`  
		Last Modified: Tue, 10 Feb 2026 18:30:50 GMT  
		Size: 76.1 MB (76138902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:128587cb08f15fb1c4799cf0cd6ff646540799ef7e8f7b2c6742e9a56a06c735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6efc748f3236de6a85bc64a623d3920e20cfa3e09f59fb56e3fb329dfafb84`

```dockerfile
```

-	Layers:
	-	`sha256:2cd7c092d904a33b072aaec071da90987ffeecc9bfb9d2da43bfcceae7768bb8`  
		Last Modified: Tue, 10 Feb 2026 18:30:48 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c86741f6f10bcb6e52c79badaa2f82c4ed52bb546f9bba305e82ff0bb445e28`  
		Last Modified: Tue, 10 Feb 2026 18:30:48 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ae25e178f950895970ac5eaf0c184df4f45702a816f9da9caf1da4ffceda28e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124719809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bcd79a5dd6dd2b27bef5f16cf2336f336e25f0e95415c8f3c0042b085db905`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:28 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:28 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:30:28 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134f14ee5011f8c88f8601f9827bdb627310b071f5f0a3b5869d4a2f4e9df5c2`  
		Last Modified: Tue, 10 Feb 2026 18:30:45 GMT  
		Size: 59.9 MB (59920333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bdfcb20d955df543e698d1c3e4c6b1706685121cf23d7122a0c4055af872a1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1158d026a59b8f3b09c2922544340eab30db5e74781eb8bcdbba1a85e9db1553`

```dockerfile
```

-	Layers:
	-	`sha256:b6b36143fb248acf34b77d4f1336012eddf8f6d1c6ed03ab6b49ccb2fb37f95f`  
		Last Modified: Tue, 10 Feb 2026 18:30:42 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963c0b3cab8b1379336cd6234df0df93e55cc6fb67f9ad73cbc39a89bd376478`  
		Last Modified: Tue, 10 Feb 2026 18:30:42 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
