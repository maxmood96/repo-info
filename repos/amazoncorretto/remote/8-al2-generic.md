## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:2112e24cdac36addf5463527632d3b7e0a6cd036fc04cb3c2029b302c55fe0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:297cba54f2cc34787b1578dd013e8481d89917cfbd6883b1b030956a7094d923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138212701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661df0cc901fbc31643754a0bfba77abdc2f1a094bad4214d2c272be9b55d1d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:22:03 GMT
COPY dir:9acefc3d435d9504bd7fba575b2c4ee96a407449bf3ba0c2338d49d9a97b2a5a in / 
# Fri, 05 Apr 2024 18:22:04 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:19:20 GMT
ARG version=1.8.0_402.b08-1
# Fri, 05 Apr 2024 19:19:42 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 19:19:43 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 19:19:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b48a4417297666404bb1459ef5f08938bfff21f2d5adb051db9f61fc54934d30`  
		Last Modified: Wed, 03 Apr 2024 01:52:33 GMT  
		Size: 62.7 MB (62667250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145437fd51067b79179f635b616cc0a3aeb2b553400916349a628f27952180a6`  
		Last Modified: Fri, 05 Apr 2024 19:34:49 GMT  
		Size: 75.5 MB (75545451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5d12c54be1d60903ab62b6e28b1306dbaedf50d8e35cd82bf7b77c7cf66eae2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124188977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b61aa8cac91bf3db40e5572f8bf19ad6101b9b52b60a5b97984dce2c44a5a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:43:15 GMT
ARG version=1.8.0_402.b08-1
# Fri, 05 Apr 2024 18:43:31 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 18:43:32 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:43:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa646d1af5c4bcd4cda7d1d93a5796974c96ea6fd6cd38c3d506fa9a9c1e1b0f`  
		Last Modified: Fri, 05 Apr 2024 18:55:17 GMT  
		Size: 59.6 MB (59628368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
