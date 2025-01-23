## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ea922f171bc0be741962c2820fa1727f8d208ba70fa8bddf241d6a125e459642
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ac1fd2ecb85b1b2309d11089b4a2b5c2458f539c8f57753619092a97746b1cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227409889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c5b52ac27f84766633f08032661a1c8666769e3d1acfd6d0d4db335a7c2eba`
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba40bee579293bea80d8fd5bf17d1160fb8b86b90eb6dc7c12a0774bb9c5df2a`  
		Last Modified: Sat, 11 Jan 2025 02:29:40 GMT  
		Size: 164.8 MB (164774059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:29f0d5b93a7d8783ed6064136c06d499412cec3ec377f3c56bf5e5ed3cdae0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef13abd39605677d01e0e80df1f4b99f9872e76c86e1081ec963e2ba90e9a52c`

```dockerfile
```

-	Layers:
	-	`sha256:16efb77f397ba4592e39a7a2cb8d951345c93915f3a83211c54336a0050efa20`  
		Last Modified: Sat, 11 Jan 2025 02:29:36 GMT  
		Size: 5.5 MB (5517001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a5f94e7558e75e06ed54bada24e86ebe7130ed14b0e47627f2e1985a4b1050`  
		Last Modified: Sat, 11 Jan 2025 02:29:35 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:185876a48ca652b810db7f5ed041f90beab05566b0423094a1b6a6a5bc0246f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227469631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080731d354a73babccdf98c9792e7af6bf1e0bfcaaee624ecd3b7697771b1aaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfe734ed07854436c37e567b57bc647f777cba775ae3377bec6f255cc7fb706`  
		Last Modified: Thu, 23 Jan 2025 18:49:48 GMT  
		Size: 162.9 MB (162879326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd38e64adcc434e6d2aa738f9860b35ffe2d2c40b19e19a9b4d160465583002e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6f06f08f75e7a93bb296be345a39675186ea72dd12dcbcc0352de0011eafab`

```dockerfile
```

-	Layers:
	-	`sha256:2d968e8b97b5076aba5aee65605c606502d64cec10e972945856ae62f02160ee`  
		Last Modified: Thu, 23 Jan 2025 18:49:43 GMT  
		Size: 5.5 MB (5515686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2e61cddc63b0fe4a088bdfd7be8603e8443254a19d431bfd9ba5efd993fd2e`  
		Last Modified: Thu, 23 Jan 2025 18:49:43 GMT  
		Size: 11.4 KB (11399 bytes)  
		MIME: application/vnd.in-toto+json
