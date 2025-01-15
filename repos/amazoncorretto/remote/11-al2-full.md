## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:136fa79276f3f980c97126b0513d6eb1e3606ec475cec89757e2fbd5348bab39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e437a0462f5a89ff7399b729c7b8d6e5dc54379681fc5d2f0550f998d385d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210817743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f710145e555e03142d57a170899fd18efe123ce0c6f69fdebaedb5ee74adc55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0c174e68d4a5429a490fb41eefc2b90cbcfb00c42e691a50f7ccf91b96b339`  
		Last Modified: Sat, 11 Jan 2025 02:29:21 GMT  
		Size: 148.2 MB (148181913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e5f17c5591548d61012a1784b44be654377e3195a9a6728d3fb3313d8e289cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa8315d0b38ace03abbfd1fe9c291c2968d73767cee866e5fefc607a1177764`

```dockerfile
```

-	Layers:
	-	`sha256:f5edd411674e47161886671a9a85ca79b9e78d8f366689dca34ac7540cb6015f`  
		Last Modified: Sat, 11 Jan 2025 02:29:19 GMT  
		Size: 5.5 MB (5524411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03963ec9585ce75b6039cd03c0abda80920cca86f0befcf580ade2c28850410`  
		Last Modified: Sat, 11 Jan 2025 02:29:18 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:696823215eb43865eb56f7fc4dcb2f261a0040243f6fce1869ef8eb74a247c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209898053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b8c691fd4eee509d234638f666eb5613d15000e7ac767ebff49ddead559c32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713f498566c0b2daecd0de1cd7dda624e9c7c87c6589c8dd1ee5e9315348b7c5`  
		Last Modified: Sat, 11 Jan 2025 02:58:49 GMT  
		Size: 145.3 MB (145307748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4eba8b75b75e5cd4990a276e41729d82f81e8106b972c92e2c00905fc3f45691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ad233b8f1ea8147859c450ae1c20ee4d553dcd95bde4ac466404975c9bcf1e`

```dockerfile
```

-	Layers:
	-	`sha256:dcb4c2d0398b7cbe4794cd359f1f2ed19efa03622984330fd0efb6d3405b78e1`  
		Last Modified: Sat, 11 Jan 2025 02:58:46 GMT  
		Size: 5.5 MB (5523905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8425ba66a73698b3f340316f9db9d6b307fa5834c7050c44605093babb5bddc`  
		Last Modified: Sat, 11 Jan 2025 02:58:45 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
