## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ab8e2d9d1536c57c3bc7d055742ea11e63eb95d9e683161470c8f5bbd1ed322f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0aecaf4d3a8cbbcd3bf733cceb29f833f45a6bff9e24093a07278a847ad8dfe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139110705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620f26d15df39511eae05af6e8ebdcfa845c3c39732658c2749215191d22b2df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:10:42 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:10:42 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:10:42 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:10:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c654e2d93482657dfab0bf439abd5feb779b96b07d19fd30e557529e414c84`  
		Last Modified: Tue, 27 Jan 2026 22:10:58 GMT  
		Size: 76.1 MB (76146996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a81f69e26eb29e2921d6f052a9e477ea36e4df0c05e6c1097d76a73bf02c52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c0ba743c25825046f7b1b38ba9d718806829d6e0ac99441ed6a8b26cf52fbf`

```dockerfile
```

-	Layers:
	-	`sha256:fd331446afb2e84c2948cc10cb26eaea7839eebaae1f1f66d3c86a676cbaae13`  
		Last Modified: Tue, 27 Jan 2026 22:10:56 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1649837a96db4cad5a90fbc7ecfe1af5ab17f84f817c3ebcbda5931d25145ed`  
		Last Modified: Tue, 27 Jan 2026 22:10:56 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3077224955dbd72484deaf8f30eb2ebbd48216c72123a9b1abe0dbc9873b700a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124719367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef19526a099c460d787249bf37a782f0d056173641ccf664455b1bd1927c806`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:10:57 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:10:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:10:57 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:10:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f2066276484af79a079da8fb7453f733eef034ca387d572b3b8569e0df47d9`  
		Last Modified: Tue, 27 Jan 2026 22:11:12 GMT  
		Size: 59.9 MB (59920478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c6e184d01ebb335eb87542a6e24e01da956e070eedad22f95feed823b4ea561d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b5423da57df0dc84cfb9f74095ead3da0e9b18c145a454028411cf251c0563`

```dockerfile
```

-	Layers:
	-	`sha256:4ee886497ef2ce5372677e04fd51b7904b4b3aa03326163df67e3ac6a17277ce`  
		Last Modified: Tue, 27 Jan 2026 22:11:10 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb66e9c42a84cd8ea7db74b8f9bdafcaaa53455a37a2d55e739d8906d43af572`  
		Last Modified: Tue, 27 Jan 2026 22:11:10 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
