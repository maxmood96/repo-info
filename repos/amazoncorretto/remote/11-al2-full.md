## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:6cdb34eeaa68c196238624e3532f8fd7300f7253d9e2fe4388197462883ca49a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f6df07c59566fa1ec85b82d2229a3a0252ec9c773838623ff98d5a040c1f99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211139640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3988c5b821d50b4ee5a4e6f78086a761ba3960df37537669cedb7bda57fa9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:08 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:08 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:08 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8a811ccc5f505f502891437310aab6cf24318c64c71d122347978d3549c18b`  
		Last Modified: Sat, 30 May 2026 01:11:29 GMT  
		Size: 148.2 MB (148197690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4887199a8b31e330b29fa5111d240ee2a89fa9a6a796a785331ac27cd7ae2f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2364458971eed7b92fdc879605dbff3db12c5995eda8874dc54664e6713cb2c8`

```dockerfile
```

-	Layers:
	-	`sha256:323eabc7b05f31761861fa9090936e4399264f8c258741738b9819ddc1c77819`  
		Last Modified: Sat, 30 May 2026 01:11:26 GMT  
		Size: 5.5 MB (5543110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ca420c1bfbad1d286016582ac1e36f057e2dd60ba21863b5b892b6accd9a47`  
		Last Modified: Sat, 30 May 2026 01:11:26 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aa353e3841e59c7071d9eb22f030413937891c3cef5a01e7031755c41e0ce30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210165168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dbe52b004486ec37a8e80803844cc2b69134e288efbb8da9f2996669c95365`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:16 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:16 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:16 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d707445c7950dfdc5fa79967c81ddc7d73770f2577e23a9b177a71ad082a73`  
		Last Modified: Sat, 30 May 2026 01:11:37 GMT  
		Size: 145.4 MB (145374459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:228d9674ae10f4f0c4540be6dc3fdecb4c06e614eeab42fdefb850cd2f8c66ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a22d4db0736563b84cf74054121db18f8d11755acfefa1f0747c6a8a868d91e`

```dockerfile
```

-	Layers:
	-	`sha256:0918c8bfd36ba14897cce01934b6892c5158810306f2fed67fb0941c411af6bc`  
		Last Modified: Sat, 30 May 2026 01:11:34 GMT  
		Size: 5.5 MB (5542604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6134d8b8039583e4b48ca0e46fce4bf355db434dda535635555fbb720edd04e9`  
		Last Modified: Sat, 30 May 2026 01:11:33 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
