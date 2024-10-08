## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:bed363f4f0d29ee5baa0ef9669739496de95583e04ffd35ec857c3b5162b9cf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5301563fd2271bfdfbf7842d46953d4d3ee26700b737201debc8ef09d95b99cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228474803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ce8096e04b928f9bd10856e63ce845b86057ae6e1c0de97f104b9680b8bddd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9853f22d8ff72bfc3a51ce0315e66e2b983c5c08c3199c216cd3e992714bf178`  
		Last Modified: Tue, 08 Oct 2024 00:00:04 GMT  
		Size: 165.8 MB (165796647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:39507b30aa28e87c2757262be90afc76ff8a204b0f0d57c40390d3a019e8a377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6115331e8c4dc27f74ec7388cbea250187edc23ec751bfd892aa3c45eb0101f`

```dockerfile
```

-	Layers:
	-	`sha256:ee054fbf3924c1030ecb00c3ffe653040fd1fa3b7c62bc63654cccc25fad0ffc`  
		Last Modified: Tue, 08 Oct 2024 00:00:01 GMT  
		Size: 5.5 MB (5527679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d91002ead44ec7b9f6117d7c727fc3e245fa7c236f7cee070536e73c42be8e`  
		Last Modified: Tue, 08 Oct 2024 00:00:01 GMT  
		Size: 11.2 KB (11218 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d42f71a1bded2cc5f9ab0c866cbe94c3684dcb013c366120d2a0fa60da0fdc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228406930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7547ea6397f82660a11881a4953e6cb0fef57047a5182811116c662dd0dfaf95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d21619c9feeafe24fc45c11645e23e593781a0a9acf5090729190d13af4a2b9`  
		Last Modified: Tue, 24 Sep 2024 02:42:43 GMT  
		Size: 163.8 MB (163820383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e9e97abee2e5516e88c870c1efe03d2202971386b568590b5952f5ee612d7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350fc7579abfc522645274ef9f80ed72e360955de8e068a62bef0a7f6f321586`

```dockerfile
```

-	Layers:
	-	`sha256:f0b8258d8aa5effed24772fcb7f7555a8d352855d156332392b84394fd69b20e`  
		Last Modified: Tue, 24 Sep 2024 02:42:38 GMT  
		Size: 5.5 MB (5526353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3f3148c810690fa989bce5ce50a08bad4b991f3c36649d6d50e412529d17fe`  
		Last Modified: Tue, 24 Sep 2024 02:42:37 GMT  
		Size: 11.6 KB (11647 bytes)  
		MIME: application/vnd.in-toto+json
