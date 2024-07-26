## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:338fa93eef2e155bb8567a5c0a2cd67dfe52d575db833a926a503d728605408d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:72219853bb46ea01bb192b85e142f9411b11b4af8cedc08c22d7ffa69ed5625f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210841245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502963265d97d9f69ca8dc5dc6ed30e15703d66b6dafc170ff6bd71608b7af49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ecb688c6985cb955c815e82b8d4331832ddeef98e9c091ce882871f77a69f`  
		Last Modified: Thu, 25 Jul 2024 21:02:25 GMT  
		Size: 148.2 MB (148162079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b17b88e13a6dd0d3a0cdf79a9ee1249b1475bdfe9bdf673030faae4d077449a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933945d623d622c0aa27ea0eb10a05c16b85d655bc8e842bf1b6083d46464e1f`

```dockerfile
```

-	Layers:
	-	`sha256:d91dc26a5896a5e9915edc761d1248bf39298ae4f2166c59fd1353b0c4d7398e`  
		Last Modified: Thu, 25 Jul 2024 21:02:21 GMT  
		Size: 5.5 MB (5535073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8a2e3aa295bad15fb8acedadd7cd8fdb954e5d5493cc5b779acbff7e349d85`  
		Last Modified: Thu, 25 Jul 2024 21:02:21 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:999f28cfabae69973e8c1df4313664cb7faaf8a97f08af719823cbabe7676abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209823613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bb951ea9525abbaa3fa8404d5e4eb2a8ae631502dda4121912623dac592093`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94ba7fc28913bc112b564ed0ed04ec4a422e4b4f163ceebd8ac29c599f9ba07`  
		Last Modified: Fri, 26 Jul 2024 01:49:40 GMT  
		Size: 145.3 MB (145250913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3cc76feb3503d72f5bc92fb540abd0abde013fa72fa68672def1168b9d0e39f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea80a4cd731ad6318f311c9d65df65cca675d4bceebba0fff372048375f8e43`

```dockerfile
```

-	Layers:
	-	`sha256:30a93bc2df52fc70ca85480c0e232feb656dc7b5ff05ab7209815bf0c100d2d2`  
		Last Modified: Fri, 26 Jul 2024 01:49:37 GMT  
		Size: 5.5 MB (5534566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3e79792511f6fd50023a1b6f15f2fa169fa0ff606d2d42ded9734c6ed04394`  
		Last Modified: Fri, 26 Jul 2024 01:49:36 GMT  
		Size: 11.7 KB (11654 bytes)  
		MIME: application/vnd.in-toto+json
