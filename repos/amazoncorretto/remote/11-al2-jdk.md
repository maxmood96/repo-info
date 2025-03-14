## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:67c910344c79db15452c4ae6ec1fa34e030c5795dcb85a5255ba7aaa6b059db0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01710340d47460ef1cc6a64940b502fb2c14a57dcf5738457a1fb7010fb01dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d740f60eb71a4f540ee3b81a59b3ad8477cb47f4f0b21526b9ce5e6d4d592c74`
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
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66d3d6094d4cd397049fc185148528c5f88b7930cf9c66ee49252ee8239250c`  
		Last Modified: Thu, 27 Feb 2025 21:08:11 GMT  
		Size: 148.3 MB (148280392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2b2bf4c3d19b9e3fc0d43fb42b3e027f976084dd61ddf9092ab197e796918d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5754ca9b91b9363f72a1e7883122f0a8dfdc4b0a1ae1c846b0548007f446643a`

```dockerfile
```

-	Layers:
	-	`sha256:bd0cb815e1b33f06d2f3a04610de751e95584c7c36d21f22977f5d76aae4c9fd`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f09bf3b98d6b1ac0672554c3828ec935ee57bbc93b3541260d4210764fc075`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
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
