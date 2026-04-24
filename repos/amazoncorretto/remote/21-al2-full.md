## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:2e49e9dd1935ea14ec8746e839987f136fb38cdb89ad66e5ab09d7f2019e0d53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8304aa30303d03d66c793285b0d14474caadd808cdfd4ab3186b8365b346ee81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228728238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0221701408348b6453be9a3da139969a0a3239a129ac1f7e5f02ca4102f887`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:20 GMT
ARG version=21.0.11.10-1
# Fri, 24 Apr 2026 00:13:20 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:13:20 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9fac6410c3c9ac2657fbeb0d603472d8240308a45a2c1714d1ca951ee5f45`  
		Last Modified: Fri, 24 Apr 2026 00:13:43 GMT  
		Size: 165.8 MB (165776055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:956fd60a652de5a2e787d52c97b0d590cdb9075370e103b687f38182474fad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d0b30f3f51a470d48e5c246f058050bbca96c056d4eae27eca02972c74a1f6`

```dockerfile
```

-	Layers:
	-	`sha256:4242f0c97e81c2bbcc6cfc3003a4baa577a108d9aac853db5cdd1e1888022473`  
		Last Modified: Fri, 24 Apr 2026 00:13:39 GMT  
		Size: 5.5 MB (5536520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaeae86b35599fb4a5dfea884ec6255f6cf7c381e3c3e2f0cf0f1386aaba8e1`  
		Last Modified: Fri, 24 Apr 2026 00:13:39 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c0102a05823a504af6dbc30ac12b8d2c1291a48422e7fc20947461c3f6753e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228691948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4666eaa2982be43dc2d35ac049793e775fcf137b62101313d6008026dec332d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:24 GMT
ARG version=21.0.11.10-1
# Fri, 24 Apr 2026 00:13:24 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:13:24 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4172a5721cede5f9312e166024bf95d5415d09c1db340145ae3aae91bfcc30`  
		Last Modified: Fri, 24 Apr 2026 00:13:51 GMT  
		Size: 163.9 MB (163893165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:39383590535ad4dd9595b6243b3d2d9e145256fefa4369f6161dba53f9441255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fa3763968b68e301765d8e6eaf9ad1ba0798ab422276cd11a13682694eba1c`

```dockerfile
```

-	Layers:
	-	`sha256:a7ad3f043ec2b0b8f45e5d0a56cda00e2e52cdc6fdb7d3da4067eac7f9566801`  
		Last Modified: Fri, 24 Apr 2026 00:13:43 GMT  
		Size: 5.5 MB (5535209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a048e1365398d85d7c5ead895d81a48a40e0675d201fb985e69bc5401abdc032`  
		Last Modified: Fri, 24 Apr 2026 00:13:43 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
