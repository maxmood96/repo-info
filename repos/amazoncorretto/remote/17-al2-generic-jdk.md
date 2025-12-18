## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:eba8935ced38cb0edcc6fd2c4e72f8ef83b23fa88fd2bcdefe52e79a8d7ab705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:242184dd81b8e8f27617914863680d5af3870c5d166a14919118a50ef0662347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18b2763794a1271ec620d362ef403138c48b0dbc8719f37294503b92ec95e48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:39 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:17:39 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:17:39 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa664a9e63598be7c33de82039c1906be50b20b21fe7be4ce3e48358cd8c570`  
		Last Modified: Thu, 18 Dec 2025 01:18:25 GMT  
		Size: 152.4 MB (152417666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7d1b640c78a09c50ff5f9a30365b2c9fb8241c599878df3784d5fca74200aa03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b17dd0dbc4689f67007589a0d5f4b75c444d07f3071852826692f70c0ca2ec0`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0fe34199980a9aa90102bdd63982bb2e1b6ea98ddb4697e78ec65b684e9e2`  
		Last Modified: Thu, 18 Dec 2025 03:29:09 GMT  
		Size: 5.5 MB (5535708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d99483e6a93b2b631de65a1800d4b8876328a4478b5ff21e0fc7678ae6eb39`  
		Last Modified: Thu, 18 Dec 2025 03:29:10 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:46b4c76651704709c3c1e500ed9aa22967b15fd284ca47288b6814ebc0722834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215784954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6afc88fdfa43f7f04bc9ecd61db1148f0e32bb3a0a59a3b7b9bc58015570fa9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:04 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:04 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:26:04 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca0a28db4df858f849233729de0ecf5383aff275c42bd9cf1d62bacb519c2c1`  
		Last Modified: Thu, 18 Dec 2025 01:26:46 GMT  
		Size: 151.0 MB (150989199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d611f4b39e603a0671c51668420dea995ec72bfd780d252fbd557a1532dc0285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e78390c933ac3e9b19a1e8ffa7e8d5acc30852b267e4777118b8ed3cb7358c3`

```dockerfile
```

-	Layers:
	-	`sha256:ebbcaefbf770fd184dfb414bae8db6a06106168d7429f063ff365a8867e5ef6d`  
		Last Modified: Thu, 18 Dec 2025 03:18:41 GMT  
		Size: 5.5 MB (5534397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a614b17e150290ffea6ddb7154e87a7fe7e599b200dcd5187524ce8f9ba2654`  
		Last Modified: Thu, 18 Dec 2025 03:18:42 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
