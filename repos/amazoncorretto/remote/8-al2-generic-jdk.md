## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:253e99170e4e483b22a0bf616918482678dd727a8937f4f124e0c8edc8d93fb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:902ac740ad87dc9c354de9b8c302695dcdbdb30816ad8e3649481fd23872a3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138279617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97297debf1bbfe72bf6cea7e986c3184e5394f444b716a6d408eec54bda8f59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd6f160fefd8d375edf6f1fb1df3872323b95d4ab484acb4428295c5977fd0`  
		Last Modified: Sat, 07 Sep 2024 01:05:46 GMT  
		Size: 75.6 MB (75584070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c743260d8ba9e0180ec56d905cc5d22938f93491fb3427830b8c9798bee49755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7cc24bff7c7d1814ff6b41b087136f654e898113313062193d6b7d1e647a2`

```dockerfile
```

-	Layers:
	-	`sha256:1f8296bb8b911472dd89315d02d5e898f907ad9ee1b01b57f9ee08a5e348a0d9`  
		Last Modified: Sat, 07 Sep 2024 01:05:45 GMT  
		Size: 5.4 MB (5369690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e38e60025aacd0de5ecc165c88ac850b8cd1788cd0f1ae64850dde81fa7152`  
		Last Modified: Sat, 07 Sep 2024 01:05:45 GMT  
		Size: 11.5 KB (11536 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

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
