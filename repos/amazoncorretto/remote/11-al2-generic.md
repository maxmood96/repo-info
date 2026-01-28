## `amazoncorretto:11-al2-generic`

```console
$ docker pull amazoncorretto@sha256:c01487a7dc9a8135b8515a7d0d36a5d664a177580831db69714c7aff74e69f5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:404a2c6e1fb99075686630c2bb5c943f267ab661f1ab25e7cf6f2eb72daed522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211094904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d6d6e92d59d5f37f0bb83a08cd67b9c6799125e395809d8b5e86d61a258d87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:41 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:12:41 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:41 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab537c006158cb59c0f5895965cca6f481a368f6abb61f4e81c796777a9eed5`  
		Last Modified: Tue, 27 Jan 2026 22:13:02 GMT  
		Size: 148.1 MB (148131195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bf33bd2146a9c4a2d95181f7567539a8c8d553d5200200f003eda91f0adab61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d265fecb5f18293d3ee74cb62fcc3018abfee84a2d6222c7246cfa3879e45504`

```dockerfile
```

-	Layers:
	-	`sha256:6d2e29ed4784afe3b6cd2a6af72c27a6ac1b8aa9dc6f50c5ffb4af25bea67214`  
		Last Modified: Tue, 27 Jan 2026 22:12:59 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71ae3f0db334ab08266f0fb76351a617a6f67574f5636d6562ee98a23718127`  
		Last Modified: Tue, 27 Jan 2026 22:12:58 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9b4e22289c973893812d7e820729c2cf276fa54009fe7601b13ab632acda97fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210023133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804259a19d92613de3621e9b064161aca9ffcf2d39ad41e9bd0586f62e4f4ba4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:39 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:11:39 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:11:39 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb2c67e2d580b2ad17d6de4766ea5018821f410e94f6e448143ef2823d1e4c8`  
		Last Modified: Tue, 27 Jan 2026 22:12:00 GMT  
		Size: 145.2 MB (145224244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f011d483dfa04d33b946dbd972260b770df10ce89c3bd51bcc98bafbb0bb27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef201ebfd3c9664f373a036233c57e7f6148c154a0de56643b993c34275f84d8`

```dockerfile
```

-	Layers:
	-	`sha256:9c8bfb8e7710528f8c01a8f8fce9f7c7b58d2ad296a64713fced6d6fd6f33420`  
		Last Modified: Tue, 27 Jan 2026 22:11:57 GMT  
		Size: 5.5 MB (5542503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42ef4f00f003dd921485de5ec7c4826983ba8f1e7d246ade084342271817d20`  
		Last Modified: Tue, 27 Jan 2026 22:11:56 GMT  
		Size: 11.4 KB (11363 bytes)  
		MIME: application/vnd.in-toto+json
