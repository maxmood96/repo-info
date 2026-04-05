## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:54a4f94aa1cc68f46fee30e82bcc8aea93ef93108a20ca020fbc3d8e0c0d5099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a41de3a12c177714d756392a12d4697550a6ed2bd48d95f635f651c28e44b4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139078856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dd7362abe649799ad32519d6982044d065e92d32ff76d5423c66e0a262394b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:11:57 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:11:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:11:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:11:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed3b592a48445e98eb3cbef3f221e49ddff0fb5de500494feceb697bdf859c`  
		Last Modified: Fri, 03 Apr 2026 22:12:13 GMT  
		Size: 76.1 MB (76123555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c7c060eab4831fb1c6e3cd3245e100c2d6123940f3d867baca0f674494117c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8beb3f425cf982944d6761476f163654b7fa48a3ad01dcbee3399317c71cd0ac`

```dockerfile
```

-	Layers:
	-	`sha256:04817d4a294747a26a942c9cf51dbc42e4cce67d9ae8239aaceabb448489defb`  
		Last Modified: Fri, 03 Apr 2026 22:12:11 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b20219fe895d4b6276145fe8ac37c8913b9830c6f77d7785a4020b861c3472`  
		Last Modified: Fri, 03 Apr 2026 22:12:11 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:44359769d87d4bc1da2b35b16a3f23d9db291a092b8a4e9ad7b0f5b89c959255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124725995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9cce2d98880dda9667a711b5c66bf4efa0c87ad3505c02f32fa2404f7d6890`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:09:58 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:09:58 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:09:58 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:09:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3d731049d7c23d3810364ce54f552fe15f577c03087e2ce9ad61877eee7ff9`  
		Last Modified: Fri, 03 Apr 2026 22:10:13 GMT  
		Size: 59.9 MB (59923156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5ddab9ecef0572f088588b15ba6a24c80e3ddf78177cda44b10a69a6ea7d07dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cccc55774ac46df3409397a3f00f0d860f5a7d26b7f8faf33963edab4d86559`

```dockerfile
```

-	Layers:
	-	`sha256:319d8a10b7c50d2e84eeed872b011d5d2e0b400093da462a82170bd963d579b7`  
		Last Modified: Fri, 03 Apr 2026 22:10:11 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee152d7992a3f33693efbcb3af2de3740a426f0df5687681d8657db58c6ee1d`  
		Last Modified: Fri, 03 Apr 2026 22:10:11 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
