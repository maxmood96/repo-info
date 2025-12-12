## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:8ad2b454056f263ab05b1e0b70e364e5231a321cee75a2c012b40a50b3d807a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0da2fddad215facd6364daac2bd7c13dacac3bfb43c0ad5e8bbf403b8de0ed08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1563cd2e9e0cc87409fd9644dccf07d01cc85f69353371ac731327ef1ae1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:25 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:25 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:25 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac57126ecd86ebc8bfbf2f8c72cef47008c2e2b42c706b3d2d81f5f916ccec5b`  
		Last Modified: Thu, 11 Dec 2025 22:13:15 GMT  
		Size: 152.4 MB (152417728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1d3ca34d0d71ba0c4c0834660f3dfdd0cc6e44044a740c6b4807466a59d6ab90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3956c673dabac0ca44a465c350bc07cb00e621f700999bbdd2e1ec9ee6925d`

```dockerfile
```

-	Layers:
	-	`sha256:6dd363252c7ed5e309e065c78284c2759d7b35acb55a3b15685b20a2c31f6f5c`  
		Last Modified: Thu, 11 Dec 2025 22:48:32 GMT  
		Size: 5.5 MB (5535708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca20732c51e39e1b6faa15c1a8d4368f2f54c1ada622847c18d1dd130143c8e`  
		Last Modified: Thu, 11 Dec 2025 22:48:33 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:732752b6c459a0b37836fe94f4eb551b1ad3b40f085d66c672e018a6ccfd9ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215784883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb62a0fa429b35437ac541d57b2d0f593af6dbb1812a0a8e3ff52ee5bc777dff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:02 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:02 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67bc37dbe272db9b7b10c3283dea952f31754f43ec167dae43bf6ef83012ea9`  
		Last Modified: Thu, 11 Dec 2025 22:12:56 GMT  
		Size: 151.0 MB (150989128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2239339cf7d5026b4711bad20f8ecf15b70da0dcd57388533b2df71e58225627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cef9561632667f731ab5d793a9021030882df098a9f685ef7e5a954b2b3a39`

```dockerfile
```

-	Layers:
	-	`sha256:08b85edcac90090634462bfc9e24cac211ebb5c5c5a184e2e4c9ef7f0064f83c`  
		Last Modified: Thu, 11 Dec 2025 22:48:38 GMT  
		Size: 5.5 MB (5534397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419654417774b296fd61227982fd46582841c50f98e8fbaf14c0fbe78d3203d9`  
		Last Modified: Thu, 11 Dec 2025 22:48:39 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
