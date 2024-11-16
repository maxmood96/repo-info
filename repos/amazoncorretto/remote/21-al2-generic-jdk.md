## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:a0734dc544ec5b57062071e867df9d31fd5f3e7550b8e8a5bd3c9a50729bc977
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f20383e9f74aae59e1bd83e2a5d81149441d8ffec053305d14d8d3069917e0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227463780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9c6e4f88b3f3129e6d9f9208d2d30877685acf10d9efae7eb1abb20e872862`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d99bf7453e16b970beb1cddf7fce76a01a106547b4a1e63679382918f788373`  
		Last Modified: Sat, 16 Nov 2024 00:48:02 GMT  
		Size: 164.8 MB (164786341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ec6ffd4bfd484f790968ee454f73383586618ba4fd57af3b18fef240472844d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daa264a4624b146da4b09544548cdee1cd0853722f1f2eb0f5573635a55491b`

```dockerfile
```

-	Layers:
	-	`sha256:4087501a1e53ddb58db6d23c9c6e767fa6cc8413418c3a4ea5fd461543b584a9`  
		Last Modified: Sat, 16 Nov 2024 00:48:00 GMT  
		Size: 5.5 MB (5527670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db1e5c9659281d04558536349b37ac6f96a394e88437f87b243588a1977b34e`  
		Last Modified: Sat, 16 Nov 2024 00:48:00 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9a483aa4e3577019b329f386d5dfbc380042fdedf0a52a17172bc54ba85c5559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227420448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147624ac6021b96ea8e43124e535678881cdabef4ab6c518faf3ce038c8a51f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12065c0a49fb98944635b5f9ab73347f950cbeb463203205939bcf365d777e`  
		Last Modified: Sat, 16 Nov 2024 01:05:33 GMT  
		Size: 162.8 MB (162838561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a845e2e85273b6a76430d67fdcd6126455818e308850658aecf578644e3108a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb26efbc142227e65715508d918b890063771abea60c356281d1fe23c229737`

```dockerfile
```

-	Layers:
	-	`sha256:0a540a09d9088c1f0b9e9c7a9da69d119fbb8aee2122379e03abd50626c38319`  
		Last Modified: Sat, 16 Nov 2024 01:05:28 GMT  
		Size: 5.5 MB (5526357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc9491ff7cda81aaf07fc59ed39807825466b051842d9bf714892bfc7a612bb6`  
		Last Modified: Sat, 16 Nov 2024 01:05:28 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
