## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:0b30fb43ca7b7041f6e97411464f68e0f49f668630417a4747db2af48c5e207a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:212007013e11f833303bca461ac80301da6ce94d4b0564f0b2733556c369a11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 MB (214709974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a549d3cc64350ce4f1a38e0e3f5696c5bb4c87c5c4e681db68a825d363c386`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82300c0b516b05fd33e5ee80103c72571455470c886da1e8007c97667bd2b934`  
		Last Modified: Fri, 04 Jul 2025 00:15:23 GMT  
		Size: 151.7 MB (151747120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c112ac15a8dbe0e761e6aec1f6a197e1b5b8761dd83c36ab835c573f19eb3c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5543728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8869a6eaee930c4dd8f39308dbe397f3e3e54f6a7217d81b4ce2aab7f749acf5`

```dockerfile
```

-	Layers:
	-	`sha256:2f6b5883bad153b9d3cea298a882362518b342eabb13a77948537cf370b74e30`  
		Last Modified: Fri, 04 Jul 2025 00:48:02 GMT  
		Size: 5.5 MB (5532473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fda6d233f5996311109c7f552ab515b802e814cb22bbc4cd03fd657e49df460`  
		Last Modified: Fri, 04 Jul 2025 00:48:02 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6fb6f38cc7b3880f9c7008e3737a7b8a2d3d09cc1e00881929782591f4d586a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215186634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72706aefa31949ea247eef69f3b84d382fe74e4df5d2fc280900971b63222a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:409bf1beed8b3d18aa6739b3b654d78ea6e9842b177c58b3fde860845eae1b51`  
		Last Modified: Wed, 25 Jun 2025 19:30:21 GMT  
		Size: 64.8 MB (64794781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee2fa749893f0ce39dd63ca3a593cb0caf15b6f548f79d56d28fac7ec9a8d3`  
		Last Modified: Fri, 04 Jul 2025 03:17:04 GMT  
		Size: 150.4 MB (150391853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61d125b6a622427e6bed6ad8bac8be3a8954de1ed90ba615b375daec5799a045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170397e6f7897ed57c981e51e0a13139b752dbcc870a4eea5625f3213dfd054a`

```dockerfile
```

-	Layers:
	-	`sha256:374dceadba3a6092a3ed87b04e436d34acd38c0b6f74bc74ef4ab0fe68f20df9`  
		Last Modified: Fri, 04 Jul 2025 03:48:01 GMT  
		Size: 5.5 MB (5531162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8f58e73dbae569c61f838183eaa62973128c1952112be35745ff96fc32921c`  
		Last Modified: Fri, 04 Jul 2025 03:48:02 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
