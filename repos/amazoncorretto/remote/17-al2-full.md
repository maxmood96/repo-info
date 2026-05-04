## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:22dc63225f186d750f61f7871717a03721d9988b3ba4ab32a54d0056efe7f7e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c8a0920483ba43aeb44df8ec319bf4550c927ae5f1baee4b7c70a63c83f50c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215469655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecc40c0c7db324551b18cfa58a196c5bf68857903ba6bb55a0d956c1623eee9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:24 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:24 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:24 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032cabcbac193a16c2253875c88ae2e3f74dab118518bde463f31531ad16461d`  
		Last Modified: Mon, 04 May 2026 20:11:45 GMT  
		Size: 152.6 MB (152609646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d254df96e21a6d3357e78e8e0e0970f8ad20f8b8beabcefa1c993b48a0a8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1438bfe32b8fb3a7232c808aef1241da3d7c5f8a3bebcf6cb720b1624f589d20`

```dockerfile
```

-	Layers:
	-	`sha256:b0991b274f1272399ae3ed9031a1d3e8c96e0b71324063a6f8e7cc0c1e0d0cff`  
		Last Modified: Mon, 04 May 2026 20:11:42 GMT  
		Size: 5.5 MB (5536617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6903103720fd6ae2a3eff1153d7e68993f21d5d9c93a1c4a3f9565d2500c632`  
		Last Modified: Mon, 04 May 2026 20:11:41 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4960e5b454c95f369f06e3f7c965bf7d148d5ecf8b007f15a86642fe36d2f8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216112277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4178bd5b7ad8cbd087fc4c40ce9e20806f6b466f8fb4949228f9f476c85d2a5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:41 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:41 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:41 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04cd62a6e78a94f951948f9a5bd7a651c4178ddc92f9efa3473eab2c4fdbe9`  
		Last Modified: Mon, 04 May 2026 20:12:03 GMT  
		Size: 151.3 MB (151316746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:296552d0b2352adabd9f8eb49609b7d46443c817807bf4832478ba64b68890fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888e964ca17e72f7508867bdd0b3740d3c384269e1fc88786732b8255ecd783a`

```dockerfile
```

-	Layers:
	-	`sha256:0f60b6954539fea6a81d76a1139a5f9a54f32f483bd1c8ef4873ada8c4a0962c`  
		Last Modified: Mon, 04 May 2026 20:12:00 GMT  
		Size: 5.5 MB (5535306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a71c1ead7c2a2101fa3155700a2171055e63765a0ca30f0f81663df6c6dc68ad`  
		Last Modified: Mon, 04 May 2026 20:11:59 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
