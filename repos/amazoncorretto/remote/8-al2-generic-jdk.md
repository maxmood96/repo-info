## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:aa177b54b86d41a1a8e59bab7365345ffc7ebb402036956d1f1083b000c55575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:38e9d47ff37adc650de66bf3cf51e20dd775db240488d9e0618a829209561ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138631386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ab7faa8ba7bcc0aecb7b697c0fb712b81df2aaec09dc5d3728a03fdb80cfee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2d47bee61bc01341abad4e3405dc5a3670b4d03bee66f04d55eefa301f8e08`  
		Last Modified: Mon, 25 Aug 2025 20:18:29 GMT  
		Size: 75.7 MB (75653261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c4100a6cb4aa373d2ea7289de7a02eea1c75a283a3d1926996f870b82f7adb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5386501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35386ad3c1940dd28c3eb1918328b4d73a10eb2d7be3429721aea017091ebbe`

```dockerfile
```

-	Layers:
	-	`sha256:c53ca431b746824390e9c3b228ac7990bd06385abc5bec0c5d1eae0fcc5ba74b`  
		Last Modified: Mon, 25 Aug 2025 21:49:54 GMT  
		Size: 5.4 MB (5374931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2639a5e380db4f3963fa858cc9e7316c80eb991f884d10f7f753823225a7fe64`  
		Last Modified: Mon, 25 Aug 2025 21:49:55 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a316ea15138fa6a28829061449e36da31bf1109348aac367f5d0465fce881f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124475578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b44c36cca70db816d11b3ef2ad257035ecc38a4118e2a1d3888a19094d602ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c2f43b8e705d2f2adc49d81efd74026f4e127df50ea79e2497e9e98bea58c`  
		Last Modified: Mon, 25 Aug 2025 22:07:58 GMT  
		Size: 59.7 MB (59674228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3455f9a30a28a1d76c69650582647184a4f0679e166d85711eb004f51710baf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5365164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4534e25bebb720594c9eff4a5d59d3605a4bbc89c2b9ad1af9d43a76cdf909b`

```dockerfile
```

-	Layers:
	-	`sha256:f4f39fc1b23dcfc75ae334df2ffae02b25a55e4de30f9d24961de3cc32a268ba`  
		Last Modified: Tue, 26 Aug 2025 00:49:52 GMT  
		Size: 5.4 MB (5353430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb73757feffc9615d814c191df076c3e1373e96c0b93ba8851509fea3b06846`  
		Last Modified: Tue, 26 Aug 2025 00:49:53 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
