## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:ea5768203e58ec38c4352a28b135c8190468e15746ee5bec6e4294dd24adf8d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:14a30d533c5d1791b5c5c11def2f20ce6a1cd5cd9ab43582d29a64b3b2e6feb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227464841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5182e717830017bb6034b785e64f183206ccacba02801b0f0c7b55c226e48bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf02143f4772415f4bc4b1e97ab9cd6cb0a41ac9a2b7602816db88b5c2317d1`  
		Last Modified: Fri, 20 Dec 2024 22:33:10 GMT  
		Size: 164.8 MB (164787402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14f3470a7d1ee7a345e50e66d628d4180d1fe14d09aad647b5a0128aedf597e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905e82d8f64b181df113d919b4ef430fc76e32388611659bb7fc57f58dfce519`

```dockerfile
```

-	Layers:
	-	`sha256:06b91c312baf82f89833f1c72fcd122bb42703aaecdfa17ee02c123bb2e3b10f`  
		Last Modified: Fri, 20 Dec 2024 22:33:07 GMT  
		Size: 5.5 MB (5517001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e306dbd98de56246fc5405582ac1f673e5dfda2d998d3e3783a25d958e66583c`  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:767d2ee6883a230f1bc24f7b1e8340ad64a358127ce86ef4e313509e0188f587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227421517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae0c87968cfa0df96a188f7ce2f5a7d180ec558bc20a0aca266a91c3aa87d69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c520393dae5bcb364385e9b1b7b5f017fd81834b93db884937ea2f00d247ab7c`  
		Size: 162.8 MB (162839630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48de806503660cf207b67529b83695dc25da1beb7dba79e913c2db68db54e130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55de31d6ee9d3c19633ca8db3f7186524ca30fa61afaf942b600d90bb511e6ab`

```dockerfile
```

-	Layers:
	-	`sha256:b38d2290d24006f464af487bcb5d1cf3fa1e7947d36dcab71a20b97bd62d700c`  
		Last Modified: Sat, 21 Dec 2024 01:49:26 GMT  
		Size: 5.5 MB (5515690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837948f19b6f3e750ef9fd7855174ebd5737237a4f3c5b18bb586a51d8adff28`  
		Last Modified: Sat, 21 Dec 2024 01:49:26 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
