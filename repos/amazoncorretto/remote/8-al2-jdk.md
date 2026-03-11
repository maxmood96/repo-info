## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ec431015a9ff2868b6ba16664ddf6e4744332a519bff9cca500c983829770aef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6a58a39f0150aa905d56da82661bf0183178d0bad85c4bdc65f524199164b2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139079886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f622b23b13be6afaea92eef99468355c3d32ef6b4dd5c3fd47dd7294c6612569`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:31:58 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:31:58 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:31:58 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d53067f2cc3fbfbaaff55c5e004564933e732b39179727b563000bbd60805`  
		Last Modified: Wed, 11 Mar 2026 18:32:14 GMT  
		Size: 76.1 MB (76123376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cade49132c64bf3b5fce81be4f6c5b7eeaf9b2d10445cf76178da42764681f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa7f755ee1165b2f4a1969eaf04f6394591ea81940269ed9e5aefe23c03b071`

```dockerfile
```

-	Layers:
	-	`sha256:08f248841146fe155440fdc6bf605aa86dcdf9a9debc4cf47977e9758d96eb00`  
		Last Modified: Wed, 11 Mar 2026 18:32:12 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82951cb80b906d50288e9e40deb416030017127831ff90cb7957cba6a84ec10c`  
		Last Modified: Wed, 11 Mar 2026 18:32:12 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e956999798ed96c176a22695980ff91c667d8e6c930b50a25976fe29b4349504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124726226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ee9f99f377b1d6ae775b7cb339e98fe53a82af536fb735eb12944e72b8ad07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:11 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:32:11 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b141cbb1d71a90eb891797bf83c37fa38a55434ccedfc7752216e35e69bfb`  
		Last Modified: Wed, 11 Mar 2026 18:32:28 GMT  
		Size: 59.9 MB (59923077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c57a2680a133a00ab13f3d7e5bb828ecdd496658480bc53b98d41e4531432e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef5774f3005e9c297b25441f17dcf01e810f86db8a2771bece55ef2769b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:a21ef5a752acc1895d8faa0daa8edc34d50bd898b5620491bac87f85f293faf5`  
		Last Modified: Wed, 11 Mar 2026 18:32:25 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4a208ae31d171b8842a6d5e722be39f342e4945e78516117d14fce315163c6`  
		Last Modified: Wed, 11 Mar 2026 18:32:24 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
