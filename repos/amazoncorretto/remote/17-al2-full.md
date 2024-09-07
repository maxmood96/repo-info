## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:4213db821a5ab7427b2b18f4c0b665de4e693478b0e545987e8c5bc61cc8c10a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a5828e6d61a9a9ecb0ac86638c7d362a7be9a892e2bc7131e3bee039664d4405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214958692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb751c3014d6936aa68d78554d7b3bb6f96cf2c773663a5d5a7a9529b8607f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387e286eea9fd83af4986c4a394dd768831fd092063ae1bece6cc56acf8d77b4`  
		Last Modified: Sat, 07 Sep 2024 01:05:56 GMT  
		Size: 152.3 MB (152263145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:572ca971f7cdac6cb9969180f724af16ded6e1ef46ad375e736b4b4fbc7554df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4e205b3cc81ba22cc9b1c238eecb8b13c573289dda1e512ad29af017d575a8`

```dockerfile
```

-	Layers:
	-	`sha256:3c6772396310eed0d8b0419ec3f3f2ac5e1322bee8b82b297c21eda197080880`  
		Last Modified: Sat, 07 Sep 2024 01:05:53 GMT  
		Size: 5.5 MB (5526954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b29105ab63b522f4d65bfcb7c05c8fe934eb3c102588963343173a51e17c50`  
		Last Modified: Sat, 07 Sep 2024 01:05:52 GMT  
		Size: 11.2 KB (11221 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:088ed3b4064baf9928bd381c441623cf346ea546f47aa0f515a2622e8f7fcb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215452328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3d8503bb8f059443eb4a725ac6356e0c7d4a3ff5cecee4c56870c19210e6d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38474b5c05d2b77230fffc123167a19f2ef0528eacc20ac5d5c44d6fd1fadfe5`  
		Last Modified: Fri, 23 Aug 2024 02:26:18 GMT  
		Size: 150.9 MB (150865193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:922ac2940112f3e3dba2af34b1ae4a8b726d686781e090214b699bde1cece70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ec71ff0c680482c94b15441d5a6815e0f6c4835d04cde80bc66e72a87f498c`

```dockerfile
```

-	Layers:
	-	`sha256:b9e34f73ec15891ef1d299e0a4a7b3d58efb8a565b0b3b0222242d04e7b5a513`  
		Last Modified: Fri, 23 Aug 2024 02:26:15 GMT  
		Size: 5.5 MB (5525641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc37c944873a61d2fed518c78deb7c32727c2376ae5f15ae0532b390ce19f43`  
		Last Modified: Fri, 23 Aug 2024 02:26:14 GMT  
		Size: 11.7 KB (11653 bytes)  
		MIME: application/vnd.in-toto+json
