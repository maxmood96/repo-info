## `amazoncorretto:8u422-al2-generic`

```console
$ docker pull amazoncorretto@sha256:d47ce558290e5a8af2e0c19d2460a2d25269e6efb645417a24c2366ccf2a2cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7a8291a115fa8b28d956c41ae6d93d15ee8df612d5b64ad63784b59e6e0feba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138246640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12316d3e685bfad86cf22d3b8118600de4bb4a63d4385e4dce5ddb87a9b69e4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e5214ca9f00993d138f174dd748df64d7c7cc31bc0c927aa036ea1cd9ca0ff`  
		Last Modified: Tue, 24 Sep 2024 02:00:32 GMT  
		Size: 75.6 MB (75568106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:147b77a8ea50fa1637906f27718269bfebdf719ea87163cc5333bc8ffe5e65dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a6f97a2ec08bc22bc976f04e2a08a3e407e82f83c1afd0f1faa1a5718aec28`

```dockerfile
```

-	Layers:
	-	`sha256:9b734f8ada2f5190d498dbdc86e1f90d7349a174828d868d6e114a7940ded4b2`  
		Last Modified: Tue, 24 Sep 2024 02:00:30 GMT  
		Size: 11.3 KB (11317 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e25e801af49fb713deb8bd055aca4043729cba70f69a2d4340ef91488110d1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124242713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68ef6348083dbe70697b2a97585a34fd76f12a7a604cfa099358ce1a38b495c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9e855b262abbb9990cf616c1a4b7f917eeb82049501e07e6b52e26e1f551dc`  
		Last Modified: Tue, 24 Sep 2024 02:26:18 GMT  
		Size: 59.7 MB (59656166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4f4ce8857a22042c4f3eda493782c63d0b891dea0e48b088c0bf2f54381d1551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41ca43de098f2fac35498936b7d850c9fac9e0167b44aef6d8594261f0a836c`

```dockerfile
```

-	Layers:
	-	`sha256:af4e824194525b7dc079337d6c3245cdef202def5362803c7bd23ab9fb2af7c0`  
		Last Modified: Tue, 24 Sep 2024 02:26:16 GMT  
		Size: 5.3 MB (5348237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43334b7e52d3bd561135d3621e818ece6d8ca1b5f2cf4c21079b919f903904a4`  
		Last Modified: Tue, 24 Sep 2024 02:26:16 GMT  
		Size: 12.0 KB (11981 bytes)  
		MIME: application/vnd.in-toto+json
