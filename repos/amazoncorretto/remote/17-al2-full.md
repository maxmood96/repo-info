## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:93325c022be96ca907c4dc590806d3d5f2d596ea300a379e971bae272405c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:39790b2a333b8803404f659c0e23887f4bb1708b01ca1225320082e349f2cb4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213807434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2828f3de3b62e485f8a912cd590143f3b5b49b77b8dc5d336db01b32eabce37`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jan 2022 02:20:04 GMT
ADD file:618cac8c5b6f6ff56ce221df12002d34997bcc996a0af3200b58db07d68be275 in / 
# Wed, 12 Jan 2022 02:20:04 GMT
CMD ["/bin/bash"]
# Wed, 19 Jan 2022 22:04:15 GMT
ARG version=17.0.2.8-1
# Wed, 19 Jan 2022 22:04:41 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 19 Jan 2022 22:04:41 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:04:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3a461b3ae562f8b6cf015b4c480a21b630a874f7fec851457680159226c81632`  
		Last Modified: Mon, 10 Jan 2022 23:29:44 GMT  
		Size: 62.2 MB (62212074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec355ba40d1bbd4a7011282af24ef6288b134d73edd7c427e6c248c1c91fd61`  
		Last Modified: Wed, 19 Jan 2022 22:14:48 GMT  
		Size: 151.6 MB (151595360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:80c062b39638247fc96adbe1af4a0c8aafad51030de2f64d3b078aec0e212a0d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214007288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2140a3f1f131fdb819e453c952f2377392300c95926f41c7d597e041f80db8f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jan 2022 02:39:41 GMT
ADD file:afc90ca87d61fdaef5c9d192a5151ab745ac8b8ea4d7544c2dfdd66bdb3b7993 in / 
# Wed, 12 Jan 2022 02:39:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Jan 2022 22:30:23 GMT
ARG version=17.0.2.8-1
# Wed, 19 Jan 2022 22:30:43 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 19 Jan 2022 22:30:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:30:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b2e274b2b0f90c3d6329566163244a0f2e6d97e4c010c62133388ac89652105f`  
		Last Modified: Wed, 12 Jan 2022 02:41:56 GMT  
		Size: 63.8 MB (63836908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e469f8ce35ae3203f14a806e3dbb74ac249cb0233c4fceab246f3123ffef25`  
		Last Modified: Wed, 19 Jan 2022 22:32:46 GMT  
		Size: 150.2 MB (150170380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
