## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:e9b9331856f7b97cfcce07b02597439e639b39ff6154a4ee50af2f4a63296128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:56010a7f0b992354d581672829459cf83387e45cb995791fe1a7284cd855391c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210978860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f723fc307e857cc93bded38e79acd0dec8d0f669a9c47a674164162fc50d12f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:16 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:16 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:11:16 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23136089a8ce8680867f05d0f4b446ef52c9f6f07586a59e6e50d65f3210aa7`  
		Last Modified: Fri, 31 Oct 2025 01:12:57 GMT  
		Size: 148.0 MB (148044792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e37cc607801296ac1366e33465681d926d4c1ff42309dfe44a0e2071ead5709f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318c0d1b88766bc0ca0d684c05a1f51f4c78eda82e98fec73bc9be4cfde834da`

```dockerfile
```

-	Layers:
	-	`sha256:b9bac7ed730546dbb10f33e1ee4e2cacad8a9c28f1a7b489fae1b14e4c88a51e`  
		Last Modified: Fri, 31 Oct 2025 03:47:20 GMT  
		Size: 5.5 MB (5543005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5899ab548058732a4c6df03bdf55f6fdcbb49cef0fd658c0ad3cbfd3c846a17d`  
		Last Modified: Fri, 31 Oct 2025 03:47:20 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3b4351890903051c079808484328af9e1f6f55a221829df3bf5799a547672cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209938179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afaee622d3d37e898d1229d38c2dafceada4d24f187afe70b13ff59d8ba7d0bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:52 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:52 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:11:52 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6cd481af92c0fe698995cb064ba61c7ee112ac206d4ce6c373a6f2da02b89`  
		Last Modified: Fri, 31 Oct 2025 01:11:02 GMT  
		Size: 145.1 MB (145144721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e4b524ecb87acc326b33cb8eb0e51c8cd1f889805ce5f09d63843ec9f5a6963c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1246c8a8ccd224edf5bd63e6fb2d50a69567d0f0a5828fcc3ee3f3cc8aca4b0`

```dockerfile
```

-	Layers:
	-	`sha256:754942db86d2ed7ca640cdc3e99f79f221ee9d34c56a8de2b6675185f27b8a5b`  
		Last Modified: Fri, 31 Oct 2025 02:16:25 GMT  
		Size: 5.5 MB (5542499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3bc9eb75d5dbdf331dd521b584db388709eaa54b82178601e1d8f536d518098`  
		Last Modified: Fri, 31 Oct 2025 02:16:26 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
