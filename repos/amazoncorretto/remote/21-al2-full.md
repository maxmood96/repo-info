## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:1ecf7a5a18a91c49286b494ef35813349655fb821743f067e0b36c4d94d18371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4fad355f170319267ff3e91a7092697798da2c0a95583af715ec10edec82161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227464131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5679b79b008eaa87d04be37e717a85b76b1b8fedab0fc0f9e9fd8f2862e8b193`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938187b8d043d01191d993a4f830d347d069880d972a1ce7b14660c4fb5460dd`  
		Last Modified: Wed, 16 Oct 2024 17:57:46 GMT  
		Size: 164.8 MB (164785975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c7ab8f58302f081d0260d2b1ff21c4a779bebf5150aab81e0a2aa14c6ce85ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b48b403037e3fac0c144813d9b11056bc1cdbb96a8960d3f1b05921b404236f`

```dockerfile
```

-	Layers:
	-	`sha256:52c93bf8c3253e8f9e45234c911759ff69849131949360da81f604cd1b54518e`  
		Last Modified: Wed, 16 Oct 2024 17:57:45 GMT  
		Size: 5.5 MB (5527683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:137a3e5212b978dc06191c6a1448e646c68e9c5f98006097624165f573cbb2b4`  
		Last Modified: Wed, 16 Oct 2024 17:57:44 GMT  
		Size: 11.3 KB (11253 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:596ea836a0e6afd5d3911d2e7758cc68eb430a923a233ee7274fb43f63311154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227433163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64653a64462a1573115eaf421f55ca1013891c3be1748caca72589fb52ca3c98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36748b1b7eead6ad7801319a0c510e15a241d9098d75d4df217e6b5a28c08099`  
		Last Modified: Wed, 16 Oct 2024 18:31:48 GMT  
		Size: 162.8 MB (162840504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9d32fd57ae08c98acf476a58a4136f119d4ef352847c790fe0547b5bffb3e1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c233cf3d78e79f746deb81c9e32c7550fd7865de6509343917fce4ea7771507`

```dockerfile
```

-	Layers:
	-	`sha256:1d3f67044960a0a8c2e0d450d3ef4788eac56068f7db99ee9e4456c7bba4b3b6`  
		Last Modified: Wed, 16 Oct 2024 18:31:44 GMT  
		Size: 5.5 MB (5526370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a395f138e8b1abb663b9845cb4b13de70731a6f2a3ed8b986a3aa8adceb3608`  
		Last Modified: Wed, 16 Oct 2024 18:31:44 GMT  
		Size: 11.4 KB (11405 bytes)  
		MIME: application/vnd.in-toto+json
