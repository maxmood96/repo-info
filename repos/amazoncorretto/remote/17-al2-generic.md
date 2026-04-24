## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:92b30e07169c235b21750fdfaa864161c07b2a1a76d89ff550df23475ce523e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dbd7ceafddcb66eadd9261f3585239f4a2360f4a8e9a05c09efa98c6fcf54ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215640583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cf3debd2393a2e8daf947ccab804693ae1c2a4ddc986833bb64da8a8bac62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:11:35 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:11:35 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:11:35 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:11:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7564beac752dec0bb235968831bc5d422be39ca32258d704c3310f0b700ee4dd`  
		Last Modified: Fri, 24 Apr 2026 00:11:56 GMT  
		Size: 152.7 MB (152688400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:771fd654c5ac728b83f12030c1a4f6b1cba08df23beabab54fe8fb008665b635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7bf8efa5946583c51c3050f66e84dd91ef68677661a2424cf6830724077ff0`

```dockerfile
```

-	Layers:
	-	`sha256:4fd326ab661e1c8e1c6dab1010c329ef9708b2e53f9044a7ef921789265b07bc`  
		Last Modified: Fri, 24 Apr 2026 00:11:52 GMT  
		Size: 5.5 MB (5536617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f5cbe4e3958d0da4d8c142e2ad12c0101a75e8ac41d56ea960c71930e77ed6`  
		Last Modified: Fri, 24 Apr 2026 00:11:51 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2797d7501fedaf8c8690cf498049a86cdcdb76218664c06e54db6b1883b9a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216110478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939008f5b6cd7adf5e461e3f06120f7bb018abbd93ddca69b49490e7b1043266`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:10:49 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:10:49 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:10:49 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:10:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976d2f926c87c0b9d8781e94d0cdcc2bf692f1538c27d2ce584358e445f69559`  
		Last Modified: Fri, 24 Apr 2026 00:11:11 GMT  
		Size: 151.3 MB (151311695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0a3f093968a196563fed8b7e7a56baec10dcd110f7a69e7406b8308aeb9b8008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02b58927d1c4a74a836d2ac33c7312e0daa480b38fb69457bcf76b4319395c3`

```dockerfile
```

-	Layers:
	-	`sha256:5c46c37da045d227ee85a514ca9d9df1ddccb2ac4a064ad61c37ad3312fc1d72`  
		Last Modified: Fri, 24 Apr 2026 00:11:07 GMT  
		Size: 5.5 MB (5535306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35cbcc7279f2a624e7586ea6620fc0031607f78efbfae6ef43761b1bc073c45a`  
		Last Modified: Fri, 24 Apr 2026 00:11:06 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
