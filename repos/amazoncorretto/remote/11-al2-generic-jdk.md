## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:593d0037c22ee8c9b04ae42a00e5da25cec8a532d90807a39e7bf5276f0781c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5b6c158ad013a0ed144fa941223e84fb80c16e190ff8ad58e33180a0ab9ab9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211263556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3df98cba18e28a5c57bc999e24e0b40f22b39330aa8f0ab2c66cf3eb94349c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efd55bb89ede17b069b01bec9bc2b63844e33bdc8fa87af7ef6ec754145581d`  
		Last Modified: Thu, 03 Jul 2025 23:13:08 GMT  
		Size: 148.3 MB (148300702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9e60b1b2def05a568f54a214e49ef07d84093dca4678b35400914002716d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd1adf6eb653335fcc63655b8841b7b40706de409c83925b6d6e0c3434bce4b`

```dockerfile
```

-	Layers:
	-	`sha256:93fb83742854075ef695d38656e8777353141dbd979451fe553e444365e80e8d`  
		Last Modified: Fri, 04 Jul 2025 00:47:18 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da0fba4c9acbc9087f51e6a24d1f6fb3a8fd8df0874d6ca400ab3558c2fb64e`  
		Last Modified: Fri, 04 Jul 2025 00:47:19 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1e55f6468de7f051dc84904b63f3e92117421e176e5e14dbfc7da1f4c851284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.1 MB (210126091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6b219eb9862be790ee0096c7d7af6cfd31f10fd1246b2a2515acef859914e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95833b4690cda234aa1b2a80bbda861c36f5508d4740f302edbd0372de994bcb`  
		Last Modified: Fri, 13 Jun 2025 21:50:50 GMT  
		Size: 145.3 MB (145335345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8200f96be890b02d29fcb9500a44d1f1b9933c6c4a23da25f9c9ed2e39725158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc6f1f705b14c765bf2aa72047da1f5d919554564699b55bb7be5bbba06de4e`

```dockerfile
```

-	Layers:
	-	`sha256:c863ff36fecb368853afaa349b3aff870d686a9413de8ef722ce315024be0af0`  
		Last Modified: Fri, 13 Jun 2025 21:47:24 GMT  
		Size: 5.5 MB (5539272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b1f508a658f0ff919ddf274da53d634274f32833804b6659c8dcb870f870d6`  
		Last Modified: Fri, 13 Jun 2025 21:47:25 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json
