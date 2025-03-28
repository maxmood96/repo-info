## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:c76603897f31c2de3a49320d93ce07168b3b87042ce9b9d8dab3337ff4bc9150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:953658250582004c1c7e4e81fc6fe447c37fdcbcde878ebef80e01730585f47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210990100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ba50a3eb428440adb964d73c07d936d03625c85e1aabe9872460af2e64452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=11.0.26.4-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279e4a4cbef7e00688d7451b377129431dee56917079ed641c490558f3d924c3`  
		Last Modified: Thu, 27 Mar 2025 23:58:33 GMT  
		Size: 148.2 MB (148237211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:66a042f9b890b3eb2110725a7efa8b0586856bc649aba26db7863677e9b06230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d08c2ab5638c5be8f741db5f0a8a820c3012cbaec24995e24c8d381a90ec36`

```dockerfile
```

-	Layers:
	-	`sha256:1148041c043efb8bef151a40ac38e7588501e70e58483b0235e7cd35a9b2a907`  
		Last Modified: Thu, 27 Mar 2025 23:58:30 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9372cfdcde35a3385b3ad6f422c7d44f18835f31ad37ba41b6fa51d0c6eb6921`  
		Last Modified: Thu, 27 Mar 2025 23:58:30 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f14547b14986fb8c6b46047dba2c97e62146bdf08fa728e778d1d4e6aab0c89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209884942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a24add8038cb68e9035bf5f47085f397bcbf12ce34c200334fd809d160c3228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d83fe85e2c73baeb609660ba452051dc9b4cd5d05b81dc306beea0a1fd531f`  
		Last Modified: Fri, 14 Mar 2025 02:25:46 GMT  
		Size: 145.3 MB (145308088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da098ebaeafeed53020eb13f5108e10847f34cf0f249c17254f6112ab95f5d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e84fa23b723b23e2010ade5165d75a7aa716d0bcc797aabf77e8dbb3dc4570b`

```dockerfile
```

-	Layers:
	-	`sha256:1f2679d4cd37e6350321a32e8bb8dfa5953529af771f34a6a6d716ff22a11fa4`  
		Last Modified: Fri, 14 Mar 2025 02:25:43 GMT  
		Size: 5.5 MB (5523909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12bb1cb1588db1b42eaa268aa1b069102eb03ba08931036d6a909a8d8977b5b5`  
		Last Modified: Fri, 14 Mar 2025 02:25:42 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
