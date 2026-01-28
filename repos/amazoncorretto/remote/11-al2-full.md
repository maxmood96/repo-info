## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:23ef1a922df2c5c548517b1ffab10b54da769d8d43cee4f4b6f9ea23fc0fc8ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:670a4d9fdeef79d036f7ec34051bd9e97e6d6d379b7800b58e9f9ba61f5309a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211094865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fe21b317a32f4b85a9d5e03a0bc8fe1e07e2000ae37ef58d1d32b3ec24dcda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:40 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:06:40 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:06:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340cef2339d12ec141de515488553d7e4c289a0b47b24df9b035a69e2a865b72`  
		Last Modified: Wed, 28 Jan 2026 04:07:00 GMT  
		Size: 148.1 MB (148131156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b9570564517483553b5af7abc6545f30241eb31c77be6f23212a4702590e37f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff2ce922b8424d6b408318c2c8ebddbe9cc765346d657c2e39fe93590146529`

```dockerfile
```

-	Layers:
	-	`sha256:cb983adb86c6fa84ba5e825643f1a3f07831d3e2ac48bac765ab4f7cbbe0e81e`  
		Last Modified: Wed, 28 Jan 2026 04:06:56 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715ef3cd9b8eb7d6cb469e9c458390733db06de451c30a7f6a9db137924adda2`  
		Last Modified: Wed, 28 Jan 2026 04:06:56 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

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

### `amazoncorretto:11-al2-full` - unknown; unknown

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
