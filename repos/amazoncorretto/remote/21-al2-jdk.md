## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ff876fc6eeac49eb64747dd10c49547532e514ef5fdd52237c1fb7a1ad77e79f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2e8f20d570b3df01b5468d029208b1ebf247caacfbe4b72a1cad2e829518407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228520268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cebdac9d4a56b205f41ebdab85aee8195346c93dfa11a7462a3ceead128ee7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:26 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:13:26 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:13:26 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4d0d315376e1ff31d7d63f3c3d4b9c25ae75c2615beb89a1ceddddb649c2b5`  
		Last Modified: Tue, 27 Jan 2026 22:13:47 GMT  
		Size: 165.6 MB (165556559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6aae34fe29a12d04229fd34b72b2aafdb87f245784798586b9f0189967a8ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a4fd2e3b2228d13f6bac83f3e442c0ad7a9e22d7a4b98f3349bc544184c9b0`

```dockerfile
```

-	Layers:
	-	`sha256:4331b80cf47173697141dbf258bc8e2d9146d5c32ae9155427de5ada63170d57`  
		Last Modified: Tue, 27 Jan 2026 22:13:43 GMT  
		Size: 5.5 MB (5535607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d97808f782225d9debca3e990c7e2ca96a8ebb531e6c710fd6f42145314b371`  
		Last Modified: Tue, 27 Jan 2026 22:13:43 GMT  
		Size: 11.2 KB (11210 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4d249785ea56883c14580cfc0f018c48d37ae90a9e33c82bcb8a72f11b9d4a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228409539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe9875f5aa587972df9204144e758424d0b346635a34657fcfdbf5d0033d178`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:25 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:12:25 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:25 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd22a6f41e63b958cc40ecbda302df5bac16126323de9b987fc0b5c42bd97e42`  
		Last Modified: Tue, 27 Jan 2026 22:12:53 GMT  
		Size: 163.6 MB (163610650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:306552acf8b02ea524197d965aa0a436707f33e14404cd352e49ee4f37b76ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c4c7f31e9a3355976f5860c9558807b6eae32a2eec646bb864ca78867ec0e5`

```dockerfile
```

-	Layers:
	-	`sha256:f7187c63d9844a45ec778c945685262c64bbd511908449260c15b8773626138d`  
		Last Modified: Tue, 27 Jan 2026 22:12:44 GMT  
		Size: 5.5 MB (5534296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6f34c14158e2fe54c494ce50218ffd3458b17d83b92f3fdc9124bdfa6cf495`  
		Last Modified: Tue, 27 Jan 2026 22:12:44 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
