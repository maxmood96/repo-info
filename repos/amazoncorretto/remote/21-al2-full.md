## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:a8405cf66c1fc0ef19dde41d5826fac11a27f98fe5164c727c862fc6a3f20de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

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
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba40bee579293bea80d8fd5bf17d1160fb8b86b90eb6dc7c12a0774bb9c5df2a`  
		Last Modified: Tue, 14 Jan 2025 20:33:14 GMT  
		Size: 164.8 MB (164774059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

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

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:65d008b395482071c2bca03be7aa8f086754ee31fa57bc77e53a3bc4cf731dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227440847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e432a65d968e5655b5a4bcac79836abc0a6b1edcf9fbf5f4289d41f80114b7`
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
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48854f99fd7ce00ff7770349e5c1ecba06bdce170ca9ed4983d3f4dc6481d497`  
		Last Modified: Tue, 14 Jan 2025 20:35:43 GMT  
		Size: 162.9 MB (162850542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:047097d2a576bde4e17936c4c15fbd316afafe3159de5e768ec095008daae132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03188d7fd9ad3f24e5f35d5c9aa7e26c2efe1283df62f8d7bdcf5f4f4c04a1d2`

```dockerfile
```

-	Layers:
	-	`sha256:c01f010aa0d72531989897610445aacfa9e2cf62422c061571afec8771393cab`  
		Last Modified: Sat, 11 Jan 2025 03:09:26 GMT  
		Size: 5.5 MB (5515690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99dcd6503f24911d33313f440d4925a5446719a4f57f43bd339fe3acf363eaae`  
		Last Modified: Sat, 11 Jan 2025 03:09:25 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
