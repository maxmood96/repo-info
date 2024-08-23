## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:6391f35e82b091c687261eaa98a2528f951b81a0d299e6bec3f27c8c6fee0ddf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:72219853bb46ea01bb192b85e142f9411b11b4af8cedc08c22d7ffa69ed5625f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210841245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502963265d97d9f69ca8dc5dc6ed30e15703d66b6dafc170ff6bd71608b7af49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ecb688c6985cb955c815e82b8d4331832ddeef98e9c091ce882871f77a69f`  
		Last Modified: Thu, 25 Jul 2024 21:02:25 GMT  
		Size: 148.2 MB (148162079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b17b88e13a6dd0d3a0cdf79a9ee1249b1475bdfe9bdf673030faae4d077449a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933945d623d622c0aa27ea0eb10a05c16b85d655bc8e842bf1b6083d46464e1f`

```dockerfile
```

-	Layers:
	-	`sha256:d91dc26a5896a5e9915edc761d1248bf39298ae4f2166c59fd1353b0c4d7398e`  
		Last Modified: Thu, 25 Jul 2024 21:02:21 GMT  
		Size: 5.5 MB (5535073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8a2e3aa295bad15fb8acedadd7cd8fdb954e5d5493cc5b779acbff7e349d85`  
		Last Modified: Thu, 25 Jul 2024 21:02:21 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:90d29d5fd2955eadd61bb837a53b099c2333f526d73296a4fe0826046713bc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209837815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06a86de390c4bdcb6db6a4ec59d9e9f7603fc54835949748bcacb4e7326407f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bd98836e44e7e42a0b707a35a7ec792c1ee849a3433e7d673d48bb5785d068`  
		Last Modified: Fri, 23 Aug 2024 02:19:38 GMT  
		Size: 145.3 MB (145250680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7bbf22220cc2e94a2437e27ed6205fed769a1dfeb3490e09098c58c9cf5dad71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bb0eb780ac70d8d2e004446f87f526c543b7441089c2b88f359a4ff3fbc473`

```dockerfile
```

-	Layers:
	-	`sha256:9653285eae1e5e2134d765732d6ca13fefb90ff318f6dc6059796fca20daea8c`  
		Last Modified: Fri, 23 Aug 2024 02:19:34 GMT  
		Size: 5.5 MB (5534582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9d9bb7d7b4de094aa20446a57c56edb3522edff48edc6c699bd5d5d643ecb7`  
		Last Modified: Fri, 23 Aug 2024 02:19:34 GMT  
		Size: 11.7 KB (11654 bytes)  
		MIME: application/vnd.in-toto+json
