## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:3efcb002c8cbaeb3faaa04191a6ee390e3e6db705afb95f05867bc28dec34a7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ba740508caa0b2681e8d1024ae6642845c3d17eab7b339cdbdbdac6fda3db95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210976547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d28135ed4f03aa380057a138247cd6c18ec858548b4d4a76e5df67c6494ec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:13 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:23:13 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab82bc1b968ff0b394b1a86c47e0c08410450fd0af9aae1698c57609f1764a6`  
		Last Modified: Wed, 03 Dec 2025 21:13:22 GMT  
		Size: 148.0 MB (148045975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c2d61f4e7934bd0fde592e813df350b90a6c83a359080bf6f7750f0d226b78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4b2f4286d6d519475da06563ee42061a22c6bbb067ea6ab6a95a8aa03aa24c`

```dockerfile
```

-	Layers:
	-	`sha256:7353c73442ad9b8e6a3e92ab87d60033720138140f0cf71d60936711dd5f8825`  
		Last Modified: Wed, 03 Dec 2025 22:47:18 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41130b98caf315fa2c162c46ccfb0fc9fbf10ff0c43b41c8dc46e3c154491209`  
		Last Modified: Wed, 03 Dec 2025 22:47:19 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6a74d3823615582a371cdbd0cefb7ff6ea26fd994d4aea8223f6c7cf2c6e6875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209937424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcac5d9d14f805dc8fb8b2f0c5ad770c5fc145703c8472048d7f2132972fef5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:31 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:27:31 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:27:31 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4f235c4ef6ec8ca62fef25256ebffc2f668944ba46fd574d65ca7a8e5337f`  
		Last Modified: Wed, 03 Dec 2025 21:13:34 GMT  
		Size: 145.1 MB (145144623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f3ceb292af74b2ada7ba419f9ead253310c6905d2837db774e4d2a9370949f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5f0a65d3f1f515e3ac6a8bd8e9563471270a5741d23ff6dda8ef3e01a81287`

```dockerfile
```

-	Layers:
	-	`sha256:67c48e80f769efeafc3daf1b6a6bfd9131b0dbb375f55ad3567cb8b1275073ef`  
		Last Modified: Wed, 03 Dec 2025 22:47:29 GMT  
		Size: 5.5 MB (5542503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454cf073fa7528a17a022bb803144654bee17bb317ac7fc647910a8d5adc29dd`  
		Last Modified: Wed, 03 Dec 2025 22:47:30 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
