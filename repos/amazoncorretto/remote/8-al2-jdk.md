## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:1d7962758401f20509cfb4526beb6be0ac94d4f787baf8f042ca1b5781df376d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d97707b6cfc5e44b9f547381cf00fa17d67a0406883bfd002e20748620cb2469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138992869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635b85659f9de487eab41d1d46742d325a87ea21befbc63ef272f1db3451eebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=1.8.0_472.b08-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3013d13d82a84e945fa3777cf596ea8fa4cd00c8b0f2b05f3750b615908887`  
		Last Modified: Tue, 21 Oct 2025 23:23:36 GMT  
		Size: 76.1 MB (76052249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7483439098617204d55d3da9792829c257d0c399853ca2b61512dacb1ca3879d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2c7a50e3f726d14c35d3b9b7087f7fcdccd4551a4b4cce2173ce0d4f5295ac`

```dockerfile
```

-	Layers:
	-	`sha256:f42bf357d514a862cf1518c0ecf323734a3851db1742c8df7a1e101e932f380e`  
		Last Modified: Wed, 22 Oct 2025 00:54:47 GMT  
		Size: 5.4 MB (5377354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455b37340352199dc1cdd30399cb0afbbccb466eb13284a6f4a1a4ca1d31c7ea`  
		Last Modified: Wed, 22 Oct 2025 00:54:47 GMT  
		Size: 11.6 KB (11569 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:94fe9d1749c0e6dbb7bafa58f4485c27a0a7cead97462138a637c8dfab9ca33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124912176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f3f5635754dd0eebc1cd644e6b7d3f2c5968c7112779eabd9e6fb568d08446`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=1.8.0_472.b08-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c88cb600be535a907eaa9dc28f559a1379c7964a2181880f693901eeb7c460`  
		Last Modified: Tue, 21 Oct 2025 21:48:51 GMT  
		Size: 60.1 MB (60118968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6aeb6437f1d4f9491c24eada1eb077951c4a3cc9ad832f8368c4ee31ff4af04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa1e49d488d097e48eafccebdd6a4651c5e1a14a7afb24e9af01ca483b2d8e6`

```dockerfile
```

-	Layers:
	-	`sha256:e1f18f7b7aad47a637388dcfaa8ce6aef2ed0e30b598fad38c5702bd297b7305`  
		Last Modified: Tue, 21 Oct 2025 23:23:45 GMT  
		Size: 5.4 MB (5355853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec37b1427143fbe2c6f07ff68941a9ff5c20837c60d1d63839f50faa2055ff9`  
		Last Modified: Tue, 21 Oct 2025 23:23:46 GMT  
		Size: 11.7 KB (11733 bytes)  
		MIME: application/vnd.in-toto+json
