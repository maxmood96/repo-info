## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:54259763281f562cae93495f8e0083517dd8841e579ffc4d1e39eac698a55dff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:67ed7200251ca1824e7e6e89fcd8a75047d0f7437f2aac1c6710480e6d266c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228070226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13922fe1d36733252b1343c7acc141ad8efee7a3ff8b9978bea305714ba543c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6d1fa18a34a0c0fc45e16116451d99d67634c7c4fc2b5fce27a221d8d5d90f`  
		Last Modified: Mon, 25 Aug 2025 20:55:08 GMT  
		Size: 165.1 MB (165092101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7cc113719be8d385ad27663b5bb8e1fd9a31d40e09976d18e0c1ea18d51de1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5543612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6e29130dea0c71c3b588c877a7812a39334874faed267819f34b6bd18c2158`

```dockerfile
```

-	Layers:
	-	`sha256:89953f0652e6376a4751749eda792433f806dd76f4c6e04de266d704a35b6e3a`  
		Last Modified: Mon, 25 Aug 2025 21:48:54 GMT  
		Size: 5.5 MB (5532364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136a97d40523d0fa651f694a420eac6d42bca5b8d6dc8f1fe1aad6fb80442c6b`  
		Last Modified: Mon, 25 Aug 2025 21:48:55 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bdb8b240d4cb8c6c9de23a4ccd619ce4a8f1ba2a84390c86e148678bb2ceab37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227908541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a609c35a53395ede66ef9cd8435bd66d618cd8fdda5358e56315ba04661b998`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aa62291cdea891fb0f6dbd4eb1ef8d998c4390d01f56ec795a31ec4bf8e23b`  
		Last Modified: Thu, 14 Aug 2025 09:20:15 GMT  
		Size: 163.1 MB (163114177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d8bcec48ed924a5d8d57e2caffe79af06a009a741ad08da45ba20412730349e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634006339308e1c0243a3db1a5ac8d6d04492d25466e292e5350da8af91d8782`

```dockerfile
```

-	Layers:
	-	`sha256:7db4d386cc24149b21401f9687582793be4a0e18d1c87901e7903dea528d37bc`  
		Last Modified: Thu, 14 Aug 2025 09:48:52 GMT  
		Size: 5.5 MB (5531053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6caeb85f12ced10956f9e49b8e5354d61af6fbc8cc74ca7dc868a698cf89c2`  
		Last Modified: Thu, 14 Aug 2025 09:48:53 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
